---
title: fmt
description: Formato de imagem de resposta. Especifica o formato de codificação de imagem para dados de imagem enviados ao cliente e o tipo MIME de resposta correspondente para o cabeçalho de resposta HTTP.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 691c5421-0754-45ce-b454-dd0ceff47a58
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '577'
ht-degree: 0%

---

# fmt {#fmt}

Formato de imagem de resposta. Especifica o formato de codificação de imagem para dados de imagem enviados ao cliente e o tipo MIME de resposta correspondente para o cabeçalho de resposta HTTP.

` fmt= *`formato`*[,[ *`pixelType`*][, *`tiffCompression`*]]`

<table id="simpletable_200779AA8D8D49A089A295AED5C98C8F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> formato </span> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>JPEG com perda. </p> </td> 
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
  <td class="stentry"> <p>png-alpha </p> </td> 
  <td class="stentry"> <p>PNG sem perda com canal alfa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif </p> </td> 
  <td class="stentry"> <p>TIFF. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>tif-alpha </p> </td> 
  <td class="stentry"> <p>TIFF com canal alfa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf </p> </td> 
  <td class="stentry"> <p>JPEG com perda incorporado em um arquivo swf do Macromedia. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>swf-alpha </p> </td> 
  <td class="stentry"> <p>JPEG com perdas e uma Máscara compactada por deflação incorporada a um arquivo swf do Macromedia. </p> </td> 
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
  <td class="stentry"> <p>gif-alpha </p> </td> 
  <td class="stentry"> <p>GIF com 255 cores mais transparência de cores-chave. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pixelType </span> </p> </td> 
  <td class="stentry"> <p>rgb </p> </td> 
  <td class="stentry"> <p>Retorna dados da imagem de RGB. </p> </td> 
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
  <td class="stentry"> <span class="varname"> tiffCompression </span> </td> 
  <td class="stentry"> <p>nenhum </p> </td> 
  <td class="stentry"> <p>Não compactado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>lzw </p> </td> 
  <td class="stentry"> <p>Compressão LZW (Lempel-Ziv-Welch) (sem perdas). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>zip </p> </td> 
  <td class="stentry"> <p>Compactação "Deflate" (sem perda). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> </p> </td> 
  <td class="stentry"> <p>jpeg </p> </td> 
  <td class="stentry"> <p>compactação JPEG (com perda). </p> </td> 
 </tr> 
</table>

*`pixelType`* Afeta a conversão do espaço de cores de saída quando `icc=` não é especificado; o perfil de cor padrão correspondente a *`pixelType`* é aplicado. Se o gerenciamento de cores estiver desativado, a conversão ingênua será aplicada. *`pixelType`* É ignorado quando `icc=` é especificado, o que determina o tipo de pixel de saída.

*`compression`* Permitido somente se tif, tif-alpha ou PDF for especificado como *`format`*. Consulte a tabela abaixo para obter as opções de compactação compatíveis com esses formatos de imagem.

`qlt-` Define as opções de codificação de JPEG para estes formatos: JPEG, TIFF com compactação de JPEG, PDF com compactação de JPEG e arquivo SWF. Use `quantize=` se `fmt=gif` ou `fmt=gif-alpha`. Consulte as descrições do comando para obter detalhes. Os outros formatos não têm opções que podem ser definidas.

Oito bits por componente de pixel são retornados para todos os formatos e tipos de pixel.

A tabela a seguir lista as combinações válidas de *`format`* e *`pixelType`*, os tipos MIME de resposta HTTP correspondentes, se os perfis ICC podem ser incorporados (consulte [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f)) e quais comandos de opção específicos de formato podem ser aplicados.

<table id="table_3461A367632E4B5A8AB578850A439024"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> <span class="varname"> formato </span> </p> </th> 
   <th colname="col2" class="entry"> <p> <span class="varname"> pixelType </span> </p> </th> 
   <th colname="col3" class="entry"> <p>Tipo de MIME de resposta </p> </th> 
   <th colname="col4" class="entry"> <p>Incorporar perfil ICC </p> </th> 
   <th colname="col5" class="entry"> <p>Opções </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>jpeg, jpg </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;imagem/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <span class="codeph"> qlt= </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, cinza </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>sim </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;imagem/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (none|lzw|zip|jpeg), pathEmbed=, qlt </span> </p> <p>( <span class="codeph"> qlt= </span> é ignorado a menos que <span class="varname"> tiffCompression </span> esteja definida como 'jpeg'.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>swf, swf-alpha </p> </td> 
   <td colname="col2"> <p>rgb, cinza </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>Não </p> <p>(O Flash Player ignora perfis ICC incorporados.) </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> atributo::TrustedDomains </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pdf </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;aplicativo/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> <span class="varname"> tiffCompression </span> </p> <p> <span class="codeph"> (none|zip|jpeg),qlt= </span> </p> <p> ( <span class="codeph"> qlt= </span> é ignorado a menos que <span class="varname"> tiffCompression </span> esteja definida como 'jpeg'.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>eps </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;imagem/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, cinza </p> <p>(Os dados são convertidos em paleta após a conversão para cinza ou rgb.) </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;imagem/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>Não </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Especifica o formato de codificação para os dados de imagem de resposta enviados ao cliente e o tipo MIME de resposta correspondente para o cabeçalho de resposta HTTP.

`png-alpha` Retorna alfa não associado (isto é, alfa não pré-multiplica os valores de pixel), enquanto `tif-alpha` e `swf-alpha` retornam alfa associado (isto é, os valores alfa são pré-multiplicados com os valores alfa). O canal alfa corresponde ao inverso da máscara de plano de fundo da vinheta para `req=img`, e à máscara de grupo ou objeto se houver `req=object`. Para aplicar alfa ao usar uma solicitação de IR aninhada, adicione `fmt=` com o formato de arquivo alfa apropriado à solicitação de IR incorporada e à solicitação principal. Nenhum dado alfa é retornado se um perfil CMYK ou ICC em tons de cinza for especificado com `icc=`.

## Propriedades {#section-eb12a82c69d84622bcea153dd84d95b3}

Pode ocorrer em qualquer lugar na solicitação.

## Padrão {#section-d2c2af11fa974e1a84e0c6cb7fb646fe}

*`format`* O padrão é `attribute::Format` e *`tiffCompression`* o padrão é `attribute::TiffEncoding`. O padrão de *`pixelType`* é `rgb` se `icc=` não for especificado, caso contrário, ele corresponde ao tipo de pixel do perfil ICC especificado.

## Consulte também {#section-c55efc881fc94c70bff91b870e026a7b}

[attribute::Format](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-format.md#reference-da5207242f1c4f1c8fa4df6027121ff2) , [attribute::JpegQuality](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-jpegquality.md#reference-d86fc5ad18bb436891efdbe1f98fea50), [attribute::TiffEncoding](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-tiffencoding.md#reference-a3425191166042d59db766c468857d0e), [qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [pathEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pathembed.md#reference-dfff01079fc74dbd896362cc740d7f5f), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb), [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38)
