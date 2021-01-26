---
description: Formato de imagem de resposta.
seo-description: Formato de imagem de resposta.
seo-title: fmt
solution: Experience Manager
title: fmt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 78ee7545-5ad9-4240-bbfc-20efe3e42ed3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---


# fmt{#fmt}

Formato de imagem de resposta.

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> format</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alfa | tif | tif-alfa | swf | pdf | gif | gif-alfa | fxg | xgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Especifica o formato de codificação de imagem para dados de imagem enviados ao cliente e o tipo MIME de resposta correspondente para o cabeçalho de resposta HTTP. </p> <p> <span class="codeph">  jpeg  </span>: JPEG com perda </p> <p> <span class="codeph"> png  </span>: PNG sem perda </p> <p> <span class="codeph"> png-alfa  </span>: PNG sem perda com canal alfa </p> <p> <span class="codeph">  tif  </span>: TIFF </p> <p> <span class="codeph"> tif-alfa  </span>: TIFF com canal alfa </p> <p> <span class="codeph">  swf  </span>: JPEG com perda incorporado em um arquivo Adobe swf </p> <p> <span class="codeph"> pdf  </span>: imagem incorporada no PDF </p> <p> <span class="codeph"> gif  </span>: GIF com 2 a 256 cores </p> <p> <span class="codeph"> gif-alfa  </span>: GIF com 2 a 255 cores mais transparência de cores chave </p> <p> <span class="codeph"> fxg  </span>: FXG com variáveis e manipulação DOM aplicada </p> <p> <span class="codeph">  fxgraw  </span>: FXG original armazenado no servidor </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb | cinza | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> Pode ser usado para afetar o espaço de cores de saída. </p> <p> <span class="codeph">  rgb  </span>: retornar dados de imagem RGB </p> <p> <span class="codeph"> cinza  </span>: retornar dados de imagem em escala cinza </p> <p> <span class="codeph"> cmyk  </span>: retornar dados de imagem CMYK </p> </td> 
 </tr> 
</table>

`tiffCompression` é permitido somente se tif, tif-alfa for especificado como o formato. Consulte a tabela abaixo para obter as opções de compactação compatíveis com esses formatos de imagem.

`qlt=` pode ser usado para definir as opções de codificação JPEG para estes formatos: JPEG, TIFF com compactação JPEG. quantize= pode ser usado se fmt=gif ou fmt=gif-alfa. Consulte as descrições dos comandos para obter detalhes. Os outros formatos não têm opções configuráveis.

8 bits por componente de pixel são retornados para todos os formatos e `pixelTypes[7]`.

A tabela a seguir lista as combinações válidas de formato e `pixelType`, os tipos MIME de resposta HTTP correspondentes.

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> format</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>Tipo MIME de resposta </p> </th> 
   <th colname="col4" class="entry"> <p>Incorporar perfil ICC </p> </th> 
   <th colname="col5" class="entry"> <p>Opções </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb, cinza, cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alfa </p> </td> 
   <td> <p>rgb, cinza </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alfa </p> </td> 
   <td> <p>rgb, cinza, cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> ( none | lzw | zip | jpeg), qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf, swf-alfa </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p><span class="codeph"> qlt=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>pdf </p> </td> 
   <td> <p>rgb, cinza, cmyk </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>yes </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alfa </p> </td> 
   <td> <p>rgb, cinza </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>not </p> </td> 
   <td> <p><span class="codeph"> quantize=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
