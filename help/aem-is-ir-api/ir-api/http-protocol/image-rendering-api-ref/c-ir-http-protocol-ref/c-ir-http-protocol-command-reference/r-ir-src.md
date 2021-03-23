---
description: Arquivo de material. Especifica dados de material, na forma de uma única referência de catálogo de material, ou como uma ou duas imagens ou arquivos de dados de material, separados por vírgula.
seo-description: Arquivo de material. Especifica dados de material, na forma de uma única referência de catálogo de material, ou como uma ou duas imagens ou arquivos de dados de material, separados por vírgula.
seo-title: src
solution: Experience Manager
title: src
uuid: 52751bcc-a65d-4441-a3b5-802d27b54b54
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---


# src{#src}

Arquivo de material. Especifica dados de material, na forma de uma única referência de catálogo de material, ou como uma ou duas imagens ou arquivos de dados de material, separados por vírgula.

`src = *``*|{{ *``*| *``*}[, *`catalogEntrymaterialFileembeddedReqMaterialFile`*]`

`srcE= *`name`*`

`srcN= *`index`*`

<table id="simpletable_A64C4F084C0A4DDCA45A921D4BD7AAEA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catalogEntry</span> </p></td> 
  <td class="stentry"> <p><span class="codeph">[/][<span class="varname"> catId</span>/]<span class="varname"> recId</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> materialFile</span> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> styleFile</span> | <span class="varname"> imageFile</span></span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> embeddedReq</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph">&amp;trace;'is&amp;lbrace;'<span class="varname"> isReq</span>'&amp;rbrace;'&amp;rbrace;|&amp;lbrace;'ir&amp;lbrace;'<span class="varname"> irReq</span>'&amp;rbrace;'|&amp;lbrace;'&amp;lbrace;'<span class="varname"> foreignReq</span>'&amp;rbrace;'</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p></td> 
  <td class="stentry"> <p>ID do catálogo de materiais (<span class="codeph"> atributo::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>Entrada do catálogo de materiais (<span class="codeph"> catálogo::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> styleFile</span> </p></td> 
  <td class="stentry"> <p>Arquivo de estilo de material (<span class="filepath"> .vnc</span> ou <span class="filepath"> .vnw</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> imageFile</span> </p></td> 
  <td class="stentry"> <p>Arquivo de dados da imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> isReq</span> </p></td> 
  <td class="stentry"> <p>Solicitação para exibição de imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> irReq</span> </p></td> 
  <td class="stentry"> <p>Solicitação para renderização de imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> foreignReq</span> </p></td> 
  <td class="stentry"> <p>Solicitação para um servidor externo. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> name</span> </p></td> 
  <td class="stentry"> <p>Nome de um material incorporado. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> index</span> </p></td> 
  <td class="stentry"> <p>Número de índice com base em 0 para um material incorporado. </p></td> 
 </tr> 
</table>

Materiais repetidos de textura, decalque e Papel de parede exigem uma única imagem, que pode ser especificada como um arquivo ou uma solicitação incorporada.

Os materiais do gabinete exigem um arquivo de estilo de gabinete ( [!DNL .vnc]), que não pode ser especificado como uma solicitação aninhada. Um arquivo de imagem de textura é opcional para gabinetes e, se especificado, pode ser um arquivo ou uma solicitação incorporada.

Os materiais de cobertura de janelas exigem um arquivo de estilo de cobertura de janela ( [!DNL .vnw]), que não pode ser especificado como uma solicitação aninhada. Um arquivo de textura é opcional e, se especificado, pode ser um arquivo ou uma solicitação incorporada.

A Renderização de imagem usa as mesmas regras que o Serviço de imagem para procurar catálogos de materiais, entradas de catálogos e arquivos de dados. Consulte a descrição do tipo de dados *`object`* na documentação do Image Serving para obter detalhes.

*`materialFile`* é um caminho relativo a  `attribute::RootPath`.

*`foreignReq`* pode ser um URL relativo a  `attribute::RootUrl`, ou um URL absoluto, se  `attribute::AllowDirectUrls` estiver definido.

Se *`catId`* não for especificado, o catálogo de sessão será usado.

`srcE=` e  `srcN=` fornecer acesso aos materiais incorporados na vinheta.

## Formatos de arquivo compatíveis {#section-f2186d3eef834fc8bbecb2bc68daacad}

A Renderização de imagem é compatível com os mesmos formatos de imagem de origem que o Dynamic Media Image Serving.

Os aplicativos que exigem dados de imagem em várias resoluções diferentes terão o melhor desempenho ao usar o formato de multiresolução TIFF (PTIFF) da pirâmide Scene7. A Exibição de imagens inclui o utilitário Conversor de imagens (IC) que cria imagens PTIFF de qualquer formato compatível.

Consulte a descrição do utilitário IC na documentação do Image Serving para obter uma lista completa dos formatos de arquivo compatíveis.

## Propriedades {#section-e68d03788d534e2184147987d51dfd0f}

Atributo de material. Obrigatório para todos os materiais, exceto a cor sólida (não permitido para materiais de cor sólida). Todas as cadeias de caracteres fazem distinção entre maiúsculas e minúsculas. *`index`* deve ser 0 ou maior.

## Padrão {#section-dde549c1917540dc8f9555962202da3c}

Nenhum.

## Exemplo {#section-675865444f8a4d35b9fc6e58b36e3438}

Um MSS para um gabinete colorido com textura repetível separada:

`…&obj=cabinets&src=cabs/maple02.vnc,cabs/maple.jpg&res=40&color=185,105,35&…`

O mesmo material pode estar localizado em um catálogo de materiais `'cat`&#39; no registro &#39; `12-3-2`&#39;:

`…&obj=cabinets&src=cat/12-3-2&…`

Uma solicitação aninhada para o Serviço de imagem para obter uma imagem de textura:

`…&obj=main&src=is{texCatalog/texture123?res=30}&res=30&…`

## Consulte também {#section-d01d25b8903e4f5ca6aef4a084fca6b7}

[Catálogos](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2) de materiais,  [atributo::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402),  [atributo::AllowDirectUrls](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-allowdirecturls.md#reference-02000c0f3c494292bad8425d06268882)
