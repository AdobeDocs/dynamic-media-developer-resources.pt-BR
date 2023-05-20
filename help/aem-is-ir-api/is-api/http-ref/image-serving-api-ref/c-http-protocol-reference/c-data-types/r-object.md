---
description: Especificador de Objeto de Origem. Os objetos de perfil de imagem, SVG e ICC podem ser especificados como entradas de catálogo de imagem ou caminhos de arquivo relativos
solution: Experience Manager
title: objeto
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 64846f8f-ebc6-446c-8277-04c45111dc24
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# objeto{#object}

Especificador de Objeto de Origem. Os objetos de perfil de imagem, SVG e ICC podem ser especificados como entradas de catálogo de imagem ou caminhos de arquivo relativos

`*`objeto`*[/]{[ *`rootId`*/] *`objId`*}| *`caminho`*`

<table id="simpletable_A8B9B4D508B94BE5B7F6112F0A5F8270"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> rootId </span> </span> </p> </td> 
  <td class="stentry"> <p>nome do catálogo de imagens ( <span class="codeph"> attribute::RootId </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objectId </span> </span> </p> </td> 
  <td class="stentry"> <p>id do registro de imagem, SVG, modelo ou perfil ICC no catálogo de imagens especificado, principal ou padrão </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> caminho </span> </span> </p> </td> 
  <td class="stentry"> <p>caminho e nome do arquivo de perfil ICC, máscara ou imagem relativa </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objeto </span> </span> </p> </td> 
  <td class="stentry"> <p>pode ocorrer no caminho do URL principal ou em um <span class="codeph"> src= </span>, <span class="codeph"> mask= </span>ou <span class="codeph"> icc= </span> comando </p> </td> 
 </tr> 
</table>

*`rootId`* identifica um catálogo de imagens. (Consulte [Catálogo de imagens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3) para obter detalhes.) Se *`rootId`* for especificado no caminho do URL, esse catálogo se tornará o *catálogo principal* para esta solicitação. Caso contrário, o catálogo padrão será usado como o catálogo principal. Vários catálogos de imagens diferentes podem ser usados na mesma solicitação.

Inicialmente, o servidor presume que *`rootId`* é omitido em `src=`, `mask=`, e `icc=` e tentará encontrar uma entrada de catálogo no catálogo principal. Efetivamente, o servidor tenta usar todo o *`object`* string como *`objId.`*

Se uma entrada de catálogo for encontrada, ela será usada; caso contrário, o servidor tentará corresponder ao *`rootId`* de um catálogo de imagens. Se um catálogo for identificado, ele será pesquisado *`objId`*. Se uma entrada for encontrada, ela será usada.

Caso contrário, *`object`* é considerado um caminho de arquivo explícito. Nesse caso, se `attribute::FullMatch` for definido no catálogo principal, o catálogo será ignorado para esse objeto e o catálogo padrão será usado no lugar dele. Se `attribute::FullMatch` não estiver definido, o catálogo principal será usado para processamento adicional.

Ambos *`rootId`* e *`objId`* fazem distinção entre maiúsculas e minúsculas. *`path`* diferencia maiúsculas e minúsculas somente no UNIX.

Se uma entrelinha `/` for especificado, o catálogo padrão será pesquisado em vez do catálogo principal. Isso é útil principalmente quando um caminho explícito requer `default::RootPath` em vez do catálogo principal `attribute::RootPath`, mas também pode ser usado para obter acesso a entradas no catálogo padrão que, de outra forma, seriam substituídas por entradas no catálogo principal.

Consulte *Gerenciamento de conteúdo* no *Guia de configuração do servidor* para obter detalhes sobre como *`path`* é traduzido para um caminho de arquivo físico.

>[!NOTE]
>
>Caracteres &#39;,&#39; de vírgula não são permitidos em *`object.`*

## Formatos de arquivo de imagem compatíveis {#section-12c85aead78e4f759856ca9ff10637d7}

Consulte a descrição do utilitário IC (Conversor de imagens) para obter uma lista completa dos formatos de arquivo suportados.

Os aplicativos que exigem dados de imagem em várias resoluções diferentes terão melhor desempenho ao usar o formato de multiresolução PTIF (Dynamic Media pyramid TIFF). O utilitário IC é usado para criar imagens PTIF a partir de qualquer formato de imagem suportado.

## Exemplos {#section-728ca9b566b54ea1afdf8f5f0a031a57}

**Acesso a uma imagem e a um perfil ICC em dois catálogos de imagens diferentes**

Recuperar a imagem &#39; [!DNL myImage]&#39; no catálogo de imagens identificado como &#39; [!DNL myCatalog]&#39; e anexar o perfil ICC &#39; [!DNL sRGB]&#39; localizado no catálogo de imagens chamado &#39; [!DNL myProfiles]&#39;:

` http:// *`server`*/myCatalog/myImage?icc=myProfiles/sRGB&iccEmbed=true`

Uso de um catálogo de imagens único com camadas

**Criar uma imagem composta simples consistindo em três camadas, todas recuperadas de &#39; [!DNL myCatalog]&#39;:**

` http:// *`server`*/myCatalog?layer=0&src=img0&layer=1&src=img1&layer=2&src=img2&wid=200`

**Acesso direto a arquivos de imagem enquanto ainda usa um catálogo para fornecer atributos**

Access [!DNL my/image/path/myImage.tif], utilizando os atributos jpg padrão configurados no `myImageCatalog`:

`http://server/myImageCatalog/my/image/path/myImage.tif?wid=200`

## Consulte também {#section-b6eccefad63f441d922699c4aba58fc9}

[Utilitário IC](../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute::FullMatch](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-fullmatch.md#reference-c3a72f31672a48b386943d6781cf50d7)
