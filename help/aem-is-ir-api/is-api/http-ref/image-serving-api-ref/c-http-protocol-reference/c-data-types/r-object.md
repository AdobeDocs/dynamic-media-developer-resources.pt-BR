---
description: Especificador do objeto de origem. Objetos de imagem, SVG e perfil ICC podem ser especificados como entradas de catálogo de imagens ou caminhos de arquivo relativos
seo-description: Especificador do objeto de origem. Objetos de imagem, SVG e perfil ICC podem ser especificados como entradas de catálogo de imagens ou caminhos de arquivo relativos
seo-title: objeto
solution: Experience Manager
title: objeto
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8d25b47d-0f23-4d9a-a7e6-6e865ae4114e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '514'
ht-degree: 0%

---


# object{#object}

Especificador do objeto de origem. Objetos de imagem, SVG e perfil ICC podem ser especificados como entradas de catálogo de imagens ou caminhos de arquivo relativos

`*``*[/]{[ *``*/] *``*}| *`objectrootIdobjIdpath`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId  </span> </span> </p> </td> 
  <td class="stentry"> <p>nome do catálogo de imagens ( <span class="codeph"> atributo::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objtId  </span> </span> </p> </td> 
  <td class="stentry"> <p>id da imagem, SVG, modelo ou registro de perfil ICC no catálogo de imagens especificado, principal ou padrão </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> caminho  </span> </span> </p> </td> 
  <td class="stentry"> <p>imagem relativa, máscara ou nome do arquivo de perfil ICC </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objeto  </span> </span> </p> </td> 
  <td class="stentry"> <p>pode ocorrer no caminho principal do URL ou em um comando <span class="codeph"> src= </span>, <span class="codeph"> mask= </span> ou <span class="codeph"> icc= </span> </p> </td> 
 </tr> 
</table>

*`rootId`* identifica um catálogo de imagens. (Consulte [Catálogo de imagens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) para obter detalhes.) Se *`rootId`* for especificado no caminho do URL, esse catálogo se tornará o *catálogo principal* desta solicitação. Caso contrário, o catálogo padrão será usado como o catálogo principal. Vários catálogos de imagem diferentes podem ser usados na mesma solicitação.

Inicialmente, o servidor presume que *`rootId`* esteja omitido nos comandos `src=`, `mask=` e `icc=` e tentará localizar uma entrada de catálogo no catálogo principal. Com efeito, o servidor tenta utilizar toda a cadeia *`object`* como *`objId.`*

Se uma entrada de catálogo for encontrada, ela será usada; caso contrário, o servidor tentará corresponder a *`rootId`* de um catálogo de imagens. Se um catálogo for identificado, ele será pesquisado por *`objId`*. Se for encontrada uma entrada, ela será usada.

Caso contrário, *`object`* será considerado um caminho de arquivo explícito. Nesse caso, se `attribute::FullMatch` estiver definido no catálogo principal, o catálogo será ignorado para esse objeto e o catálogo padrão será usado. Se `attribute::FullMatch` não estiver definido, o catálogo principal será usado para processamento adicional.

Ambos *`rootId`* e *`objId`* fazem distinção entre maiúsculas e minúsculas. *`path`* faz distinção entre maiúsculas e minúsculas somente no UNIX.

Se um &#39;/&#39; à esquerda for especificado, o catálogo padrão será pesquisado em vez do catálogo principal. Isso é útil principalmente quando um caminho explícito requer `default::RootPath` em vez de `attribute::RootPath` do catálogo principal, mas também pode ser usado para obter acesso a entradas no catálogo padrão que, de outra forma, seriam substituídas por entradas no catálogo principal.

Consulte *Managing Content* no *Server Configuration Guide* para obter detalhes sobre como *`path`* é traduzido para um caminho de arquivo físico.

>[!NOTE]
>
>Caracteres de vírgula &#39;,&#39; não são permitidos em *`object.`*

## Formatos de arquivo de imagem suportados {#section-12c85aead78e4f759856ca9ff10637d7}

Consulte a descrição do utilitário IC (Image Converter) para obter uma lista completa dos formatos de arquivo suportados.

Os aplicativos que exigem dados de imagem em várias resoluções diferentes terão melhor desempenho ao usar o formato de multiresolução TIFF (PTIF) da pirâmide Dynamic Media. O utilitário IC é usado para criar imagens PTIF a partir de qualquer formato de imagem compatível.

## Exemplos {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Acessar uma imagem e um perfil ICC em dois catálogos de imagens diferentes**

Recupere a imagem &#39; [!DNL myImage]&#39; no catálogo de imagens identificado como &#39; [!DNL myCatalog]&#39; e anexe o perfil ICC &#39; [!DNL sRGB]&#39; localizado no catálogo de imagens chamado &#39; [!DNL myProfiles]&#39;:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Uso de um único catálogo de imagens com camadas

**Crie uma imagem composta simples formada por três camadas, todas recuperadas de &#39;  [!DNL myCatalog]&#39;:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Acessar arquivos de imagem diretamente enquanto ainda usa um catálogo para fornecer atributos**

Acesse [!DNL my/image/path/myImage.tif], usando os atributos jpg padrão configurados em `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Consulte também {#section-b6eccefad63f441d922699c4aba58fc9}

[Utilitário](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b) IC,  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [atributo::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
