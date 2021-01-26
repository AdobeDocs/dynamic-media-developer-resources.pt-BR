---
description: Propriedades de dados de resposta. Avalia a solicitação atual como se fosse uma solicitação de imagem (req=img), mas em vez de retornar a imagem, o servidor retorna as propriedades selecionadas da imagem de resposta.
seo-description: Propriedades de dados de resposta. Avalia a solicitação atual como se fosse uma solicitação de imagem (req=img), mas em vez de retornar a imagem, o servidor retorna as propriedades selecionadas da imagem de resposta.
seo-title: props
solution: Experience Manager
title: props
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b9325654-81d6-4f00-bf0a-36650bea6b8d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 0%

---


# props{#props}

Propriedades de dados de resposta. Avalia a solicitação atual como se fosse uma solicitação de imagem (req=img), mas em vez de retornar a imagem, o servidor retorna as propriedades selecionadas da imagem de resposta.

` req=props[,text|javascript|xml|{json[&id= *`reqId`*}]`

<table id="simpletable_A9FCC880171B4A9DBAE28413AFDF75F7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> reqId  </span> </span> </p> </td> 
  <td class="stentry"> <p>Identificador de solicitação exclusivo. </p> </td> 
 </tr> 
</table>

As solicitações compatíveis com o formato de resposta JSONP permitem que você especifique o nome do manipulador de retorno de chamada JS usando a sintaxe estendida do parâmetro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` é o nome do manipulador JS presente na resposta JSONP. Somente caracteres a-z, A-Z e 0-9 são permitidos. Opcional. O padrão é `s7jsonResponse`.

Consulte [Propriedades](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9) para obter uma descrição da sintaxe de resposta e do tipo MIME de resposta. A resposta HTTP pode ser armazenada em cache com um TTL baseado em `attribute::NonImgExpiration`.

As seguintes propriedades são retornadas para solicitações /is/image:

<table id="table_9665612ED7D24C07AAF75D953C0FEB36"> 
 <tbody> 
  <tr> 
   <td> <b> Propriedade</b> </td> 
   <td> <b> Tipo</b> </td> 
   <td> <b> Descrição</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.bgc  </span> </p> </td> 
   <td> <p> hexadecimal </p> </td> 
   <td> <p> Cor do plano de fundo (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88" type="reference" format="dita" scope="local"> bgc= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td valign="top"> <p> <span class="codeph"> image.height  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Responder altura da imagem em pixels </p> </td> 
  </tr> 
  <tr> 
   <td valign="top"> <p> <span class="codeph"> image.iccEmbed  </span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> True se o perfil ICC estiver incorporado na imagem de resposta. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e" type="reference" format="dita" scope="local"> IccEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.iccProfile  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Nome/descrição do perfil associado à imagem de resposta. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.length  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Tamanho da resposta em pixels que não incluem o cabeçalho HTTP; 0 se os dados da imagem de resposta não tiverem sido armazenados em cache anteriormente pelo servidor. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76" type="reference" format="dita" scope="local"> req=loadcache </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.mask  </span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> 1 se a imagem de resposta incluir um canal alfa, caso contrário, 0. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pixTyp  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> O tipo de imagem de resposta pode ser <span class="codeph"> CMYK </span>, <span class="codeph"> RGB </span> ou <span class="codeph"> BW </span> (para imagens em escala cinza). </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.pathEmbed  </span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 se a imagem de resposta incorporar quaisquer caminhos, caso contrário, 0. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301" type="reference" format="dita" scope="local"> pathEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.printRes  </span> </p> </td> 
   <td> <p> real </p> </td> 
   <td> <p> Resolução de impressão (dpi) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.quality  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Qualidade JPEG. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352" type="reference" format="dita" scope="local"> qlt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.type  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Tipo de MIME para a imagem de resposta. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a" type="reference" format="dita" scope="local"> fmt= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.width  </span> </p> </td> 
   <td> <p> integer </p> </td> 
   <td> <p> Largura da imagem de resposta em pixels. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.xmpEmbed  </span> </p> </td> 
   <td> <p> booleano </p> </td> 
   <td> <p> 1 se a imagem de resposta incorporar dados xmp, caso contrário, 0. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-xmpembed.md#reference-46ecf40a40a0442fa62de3a85dcb03e8" type="reference" format="dita" scope="local"> xmpEmbed= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> image.version  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Identificador da versão da imagem. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>.) </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> metadata.version  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Identificador da versão de metadados. (Consulte <span class="codeph"> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-id.md#reference-60661184deb3420998779724244fcfa0" type="reference" format="dita" scope="local"> id= </a> </span>.) </p> </td> 
  </tr> 
 </tbody> 
</table>

As seguintes propriedades são retornadas para solicitações `/is/content`:

<table id="table_B66360C475CE495D9701AB526E758873"> 
 <tbody> 
  <tr> 
   <td> <b> Propriedade</b> </td> 
   <td> <b> Tipo</b> </td> 
   <td> <b> Descrição</b> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> caminho  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p>Caminho de arquivo parcialmente resolvido. (Consulte <span class="codeph"> static::Path </span>.) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> length </span> </p> </td> 
   <td> <p> int </p> </td> 
   <td> <p> Tamanho do arquivo de objeto em bytes </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> expiração  </span> </p> </td> 
   <td> <p> duplo </p> </td> 
   <td> <p> <span class="codeph"> static::Expiração  </span> ou o tempo padrão para a vida </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> lastModified  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> Data/hora de modificação (de <span class="codeph"> static::TimeStamp </span> ou o arquivo de objeto) </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> userType  </span> </p> </td> 
   <td> <p> string </p> </td> 
   <td> <p> <span class="codeph"> static::UserType  </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

