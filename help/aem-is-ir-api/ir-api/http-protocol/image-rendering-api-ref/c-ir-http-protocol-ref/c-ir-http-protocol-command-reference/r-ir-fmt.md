---
description: Formato de imagem de resposta. Especifica o formato de codificação de imagem para os dados de imagem enviados ao cliente e o tipo MIME de resposta correspondente para o cabeçalho de resposta HTTP.
seo-description: Formato de imagem de resposta. Especifica o formato de codificação de imagem para os dados de imagem enviados ao cliente e o tipo MIME de resposta correspondente para o cabeçalho de resposta HTTP.
seo-title: fmt
solution: Experience Manager
title: fmt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7c589119-d1b3-460f-acbd-5e8d10d0d976
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---


# fmt{#fmt}

Formato de imagem de resposta. Especifica o formato de codificação de imagem para os dados de imagem enviados ao cliente e o tipo MIME de resposta correspondente para o cabeçalho de resposta HTTP.

` fmt= *``*[,[ *``*][, *`formatpixelTypetiffCompression`*]]`

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> format  </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG sinistro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpg </p> </td> 
  <td class="stentry"> <p>JPG com perda. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png </p> </td> 
  <td class="stentry"> <p>PNG sem perda. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>png-alfa </p> </td> 
  <td class="stentry"> <p>PNG sem perda com canal alfa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alfa </p> </td> 
  <td class="stentry"> <p>TIFF com canal alfa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>JPEG com perda incorporado em um arquivo swf do Macromedia. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alfa </p> </td> 
  <td class="stentry"> <p>JPEG com perda e uma máscara compactada em deflate incorporada a um arquivo swf do Macromedia. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>pdf </p> </td> 
  <td class="stentry"> <p>Imagem incorporada no PDF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>eps </p> </td> 
  <td class="stentry"> <p>PostScript Encapsulado binário descompactado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif </p> </td> 
  <td class="stentry"> <p>GIF com 256 cores. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>gif-alfa </p> </td> 
  <td class="stentry"> <p>GIF com 255 cores mais transparência de cores chave. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType  </span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>Retorna dados de imagem RGB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cinza </p> </td> 
  <td class="stentry"> <p>Retorna dados de imagem em tons de cinza. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>cmyk </p> </td> 
  <td class="stentry"> <p>Retorna dados de imagem CMYK. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <span class="varname"> tiffCompression  </span> </td> 
  <td class="stentry"> <p>none </p> </td> 
  <td class="stentry"> <p>Descompactado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
  <td class="stentry"> <p>Compactação LZW (Lempel-Ziv-Welch) (sem perdas). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>Compactação "Deflate" (sem perdas). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>Compactação JPEG (com perdas). </p> </td> 
 </tr> 
</table>

*`pixelType`* conversão do espaço de cor de saída de efeitos quando não  `icc=` for especificada; o perfil de cor padrão correspondente a  *`pixelType`* é aplicado. Se o gerenciamento de cores estiver desativado, a conversão ingênua será aplicada. *`pixelType`* é ignorada quando  `icc=` é especificada, o que determina o tipo de pixel de saída.

*`compression`* é permitido somente se tif, tif-alfa ou PDF for especificado como o  *`format`*. Consulte a tabela abaixo para obter as opções de compactação compatíveis com esses formatos de imagem.

`qlt-` define as opções de codificação JPEG para estes formatos: JPEG, TIFF com compactação JPEG, PDF com compactação JPEG e arquivo SWF. Use `quantize=` se `fmt=gif` ou `fmt=gif-alpha`. Consulte as descrições dos comandos para obter detalhes. Os outros formatos não têm opções configuráveis.

8 bits por componente de pixel são retornados para todos os formatos e tipos de pixels.

A tabela a seguir lista as combinações válidas de *`format`* e *`pixelType`*, os tipos MIME de resposta HTTP correspondentes, se os perfis ICC podem ser incorporados (consulte [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)) e quais comandos de opção específicos de formato podem ser aplicados.

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> format  </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType  </span> </p> </th> 
   <th colname="col3" class="entry"> <p>Tipo MIME de resposta </p> </th> 
   <th colname="col4" class="entry"> <p>Incorporar Perfil ICC </p> </th> 
   <th colname="col5" class="entry"> <p>Opções </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt=  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png-alfa </p> </td> 
   <td colname="col2"> <p>rgb, cinza </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8, png8-alfa </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>yes </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif, tif-alfa </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression  </span> </p> <p> <span class="codeph"> (none|lzw|zip|jpeg), pathEmbed=, qlt  </span> </p> <p>( <span class="codeph"> qlt= </span> é ignorada, a menos que <span class="varname"> tiffCompression </span> seja definido como 'jpeg'.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf, swf-alfa </p> </td> 
   <td colname="col2"> <p>rgb, cinza </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Não </p> <p>(O Flash Player ignora perfis ICC incorporados.) </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>,  <span class="codeph"> atributo::TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression  </span> </p> <p> <span class="codeph"> (nenhum|zip|jpeg),qlt=  </span> </p> <p> ( <span class="codeph"> qlt= </span> é ignorada, a menos que <span class="varname"> tiffCompression </span> seja definido como 'jpeg'.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eps </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif, gif-alfa </p> </td> 
   <td colname="col2"> <p>rgb, cinza </p> <p>(Os dados são convertidos em paleta após conversão em cinza ou em rgb.) </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Não </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Especifica o formato de codificação para dados de imagem de resposta enviados ao cliente e o tipo MIME de resposta correspondente para o cabeçalho de resposta HTTP.

`png-alpha` retorna alfa não associado (ou seja, alfa não multiplica os valores de pixel), enquanto  `tif-alpha`e  `swf-alpha` retorna alfa associado (ou seja, os valores alfa são pré-multiplicados com os valores alfa). O canal alfa corresponde ao inverso da máscara de plano de fundo da vinheta para `req=img` e ao grupo ou à máscara de objeto no caso de `req=object`. Para aplicar alfa ao usar uma solicitação IR aninhada, adicione `fmt=` com o formato de arquivo alfa apropriado à solicitação IR incorporada e à solicitação principal. Nenhum dado alfa será retornado se um perfil CMYK ou ICC em tons de cinza for especificado com `icc=`.

## Propriedades {#section-eb12a82c69d84622bcea153dd84d95b3}

Pode ocorrer em qualquer lugar na solicitação.

## Padrão {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* padrão  `attribute::Format`e  *`tiffCompression`* padrão  `attribute::TiffEncoding`. *`pixelType`* o padrão é  `rgb` se não  `icc=` for especificado, caso contrário, corresponde ao tipo de pixel do perfil ICC especificado.

## Consulte também {#section-c55efc881fc94c70bff91b870e026a7b}

[atributo::Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) ,  [atributo::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50),  [atributo::TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e),  [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd),  [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f),  [ ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f)  [ ](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)  [pathEmbed=, req=, quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
