---
description: Formato de imagem de resposta.
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e179fc51-0461-4000-99eb-4390c35d5606
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---

# fmt{#fmt}

Formato de imagem de resposta.

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> formato</span> </span> </p></td> 
  <td class="stentry"> <p>JPEG <span class="codeph"> | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Especifica o formato de codificação de imagem para dados de imagem enviados ao cliente e o tipo MIME de resposta correspondente para o cabeçalho de resposta HTTP. </p> <p> <span class="codeph"> jpeg </span>: JPEG com perdas </p> <p> <span class="codeph"> png </span>: PNG sem perda </p> <p> <span class="codeph"> png-alpha </span>: PNG sem perda com canal alpha </p> <p> <span class="codeph"> tif </span>: TIFF </p> <p> <span class="codeph"> tif-alpha </span>: TIFF com canal alpha </p> <p> <span class="codeph"> swf </span>: JPEG com perdas incorporado em um arquivo swf de Adobe </p> <p> <span class="codeph"> pdf </span>: imagem incorporada no PDF </p> <p> <span class="codeph"> gif </span>: GIF com 2 a 256 cores </p> <p> <span class="codeph"> gif-alpha </span>: GIF com 2 a 255 cores mais transparência de cor de chave </p> <p> <span class="codeph"> fxg </span>: FXG com variáveis e manipulação de DOM aplicada </p> <p> <span class="codeph"> fxgraw </span>: FXG original armazenado no servidor </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">rgb | cinza | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Pode ser usado para afetar o espaço de cores de saída. </p> <p> <span class="codeph"> rgb </span>: retornar dados da imagem RGB </p> <p> <span class="codeph"> cinza </span>: retornar dados de imagem em tons de cinza </p> <p> <span class="codeph"> cmyk </span>: retornar dados de imagem CMYK </p> </td> 
 </tr> 
</table>

`tiffCompression` é permitido somente se tif, tif-alpha é especificado como o formato. Consulte a tabela abaixo para obter as opções de compactação compatíveis com esses formatos de imagem.

`qlt=` pode ser usado para definir as opções de codificação de JPEG para estes formatos: JPEG, TIFF com compactação JPEG. quantize= pode ser usado se fmt=gif ou fmt=gif-alpha. Consulte as descrições do comando para obter detalhes. Os outros formatos não têm opções que podem ser definidas.

O componente de 8 bits por pixel é retornado para todos os formatos e `pixelTypes[7]`.

A tabela a seguir lista as combinações válidas de formato e `pixelType`, os tipos MIME de resposta HTTP correspondentes.

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> formato</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>Tipo de MIME de resposta </p> </th> 
   <th colname="col4" class="entry"> <p>Incorporar perfil ICC </p> </th> 
   <th colname="col5" class="entry"> <p>Opções </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb, cinza, cmyk </p> </td> 
   <td> <p>&lt;image/jpeg&gt; </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alpha </p> </td> 
   <td> <p>rgb, cinza </p> </td> 
   <td> <p>&lt;image/png&gt; </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alpha </p> </td> 
   <td> <p>rgb, cinza, cmyk </p> </td> 
   <td> <p>&lt;image/tiff&gt; </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> ( nenhum | lzw | zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf, swf-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application/x-shockwave-flash&gt; </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p><span class="codeph"> qlt= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb, cinza, cmyk </p> </td> 
   <td> <p>&lt;application/pdf&gt; </p> </td> 
   <td> <p>sim </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alpha </p> </td> 
   <td> <p>rgb, cinza </p> </td> 
   <td> <p>&lt;image/gif&gt; </p> </td> 
   <td> <p>não </p> </td> 
   <td> <p><span class="codeph"> quantize=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
