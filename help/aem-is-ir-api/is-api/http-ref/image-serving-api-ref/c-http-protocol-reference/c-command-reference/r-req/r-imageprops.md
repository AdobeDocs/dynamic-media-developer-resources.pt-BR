---
description: Propriedades da imagem de origem. Retorna as propriedades selecionadas do arquivo de imagem ou da entrada de catálogo especificada no caminho do URL.
solution: Experience Manager
title: imageprops
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b4337c20-8e47-4d61-b234-19434f5c5216
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 0%

---

# imageprops{#imageprops}

Propriedades da imagem de origem. Retorna as propriedades selecionadas do arquivo de imagem ou da entrada de catálogo especificada no caminho do URL.

`req=imageprops[,text|javascript|xml|{json[&id= *`reqId`*]}]`

<table id="simpletable_8E03127D50444CA7878A6B08E866EE2E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p> </td> 
  <td class="stentry"> <p>Identificador exclusivo da solicitação. </p></td> 
 </tr> 
</table>

A resposta HTTP pode ser armazenada em cache com o TTL com base em `attribute::NonImgExpiration`.

Outros comandos na cadeia de caracteres de solicitação são ignorados.

As solicitações que oferecem suporte ao formato de resposta JSONP permitem especificar o nome do manipulador de retorno de chamada JS usando a sintaxe estendida de `req=` parâmetro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.

As seguintes propriedades são retornadas:

<table id="table_5F289E2E21594A5598DF98E65DEDDFA0"> 
 <tbody> 
  <tr> 
   <td> <b> Propriedade</b> </td> 
   <td> <b> Tipo</b> </td> 
   <td> <b> Descrição</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.anchor</span> </p> </td> 
   <td> <p> int,int </p> </td> 
   <td> <p> <span class="codeph"> catálogo::Âncora</span> ou o ponto de ancoragem padrão </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.expiration</span> </p> </td> 
   <td> <p> duplo </p> </td> 
   <td> <p> <span class="codeph"> catálogo::Expiração</span> ou o tempo de vida padrão </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.height</span> </p> </td> 
   <td> <p> inteiro </p> </td> 
   <td> <p>Altura da imagem com resolução total em pixels </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.iccProfile</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Nome/descrição do perfil associado a esta imagem </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> imagem. embeddedIccProfile</span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 se o perfil associado estiver incorporado na imagem </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.embedded PhotoshopPaths</span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 se a imagem incluir dados de caminho do Photoshop </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> imagem. embeddedXmpData</span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 se a imagem incluir dados XMP </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.mask</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 0 para nenhuma máscara, 1 para alfa pré-multiplicado, 2 para alfa não pré-multiplicado e 3 para uma imagem de máscara separada </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.modifier</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> catálogo::Modificador</span> ou vazio se não for uma entrada de catálogo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> imagem. photoshopPathNames</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Lista separada por vírgulas dos nomes de todos os caminhos do Photoshop associados a esta imagem </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.pixType</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Tipo de imagem, pode ser 'CMYK', 'RGB' ou 'BW' (para imagens em tons de cinza) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.postModifier</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> attribute::PostModifier</span> ou vazio se não for uma entrada de catálogo </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.printRes</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> resolução de impressão padrão em pixels/polegada </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.resolution</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> catálogo::Resolução</span> ou a resolução de objeto padrão </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.timeStamp</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p>Data/hora de modificação (de <span class="codeph"> catálogo::Carimbo de data/hora</span> ou o arquivo de imagem) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbRes</span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> <span class="codeph"> catálogo::ThumbRes</span> ou a resolução de miniatura padrão </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.thumbType</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> catálogo::ThumbType</span> ou o tipo de miniatura padrão </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.width</span> </p> </td> 
   <td> <p> inteiro </p> </td> 
   <td> <p> Largura da imagem com resolução total em pixels </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> image.convertedId</span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> ID do catálogo para o qual o <span class="varname"> objeto</span> especificado no caminho é resolvido (consulte <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md#reference-cf3e34e6cbb346d69ded9982bfdef414" type="reference" format="dita" scope="local"> Conversão Da Id Do Objeto</a>). </p> </td> 
  </tr> 
 </tbody> 
</table>
