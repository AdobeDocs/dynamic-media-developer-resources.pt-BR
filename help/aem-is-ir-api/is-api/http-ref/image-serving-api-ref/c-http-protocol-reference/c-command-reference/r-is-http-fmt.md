---
description: Formato de imagem de resposta.
seo-description: Formato de imagem de resposta.
seo-title: fmt
solution: Experience Manager
title: fmt
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 29151740-3bbc-4c5e-bbc7-4afe9064ff5f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 0%

---


# fmt{#fmt}

Formato de imagem de resposta.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* — jpeg | jpg | pjpeg | png | png8 | png-alfa | png8-alfa | tif | tif-alfa | swf | swf-alfa | swf3 | swf3-alfa | eps | gif | gif-alfa | m3u8 | f4m | Web | webp-alfa | jpeg2000 | jpeg2000-alfa | jpegxr | jpegxr-alfa

| *`format`* | Descrição |
|---|---| 
| `jpeg` | JPEG com perdas |
| `jpg` | JPG com perda |
| `pjpeg` | JPEG progressivo |
| `png` | PNG sem perdas de 24 bits |
| `png8` | PNG sem perdas de 8 bits |
| `png-alpha` | PNG sem perdas de 24 bits com canal alfa |
| `png8-alpha` | PNG sem perdas de 8 bits com canal alfa |
| `tif` | TIFF |
| `tif-alpha` | TIFF com canal alfa |
| `pdf` | Imagem incorporada no PDF |
| `eps` | PostScript binário encapsulado não compactado |
| `gif` | GIF com 2 a 256 cores |
| `gif-alpha` | GIF com 2 a 255 cores mais transparência de cores chave |
| `swf` | JPEG com perdas incorporado em um arquivo swf do Adobe AS2 |
| `swf-alpha` | JPEG com perdas e uma máscara compactada deflate incorporada em um arquivo swf do Adobe AS2 |
| `swf3` | JPEG com perdas incorporado em um arquivo swf do Adobe AS3 |
| `swf3-alpha` | JPEG com perda e uma máscara compactada em deflate incorporada a um arquivo swf do Adobe AS3. **Observação**: os formatos swf e swf-alfa são mais bem usados para aplicativos do ActionScript 2 (Flash Player 8 e anterior). swf3 e swf3-alfa são recomendados para uso em aplicativos ActionScript3 (Flash Player 9 e posterior) |
| `m3u8` | Formato de manifesto do Apple Streaming Server |
| `f4m` | Formato de manifesto do Servidor de Streaming do Flash |
| `webp` | WebP sem perdas e com perdas |
| `webp-alpha` | WebP com perda e perda com canal alfa |
| `jpeg2000` | JPEG 2000 com perdas e perdas |
| `jpeg2000-alpha` | JPEG 2000 com canal alfa com perda e perda |
| `jpegxr` | JPEG XR com perdas e perdas |
| `jpegxr-alpha` | JPEG XR com canal alfa com perda e perda |


| *`pixelType`* — rgb | cinza | cmyk |
| *`pixelType`* | Descrição |
|---|---|
| `rgb` | Retorna dados de imagem RGB. |
| `gray` | Retorna dados de imagem em tons de cinza. |
| `cmyk` | Retorna dados de imagem CMYK. |

| *`compression`* — none | lzw | zip | jpeg | perda | sem perdas |
| *`compression`* | Descrição |
|---|---|
| `none` | Descompactado |
| `lzw` | Compactação LZW (Lempel-Ziv-Welch) (sem perdas) |
| `zip` | Compactação &quot;Deflate&quot; (sem perdas) |
| `jpeg` | Compactação JPEG (com perda) |
| `lossy` | Compactação WebP, JPEG 2000 e JPEG XR (com perdas) |
| `lossless` | Compactação WebP, JPEG 2000 e JPEG XR (sem perdas) |

* *`format`* especifica o formato de codificação de imagem para os dados de imagem enviados ao cliente e o tipo MIME de resposta correspondente para o cabeçalho de resposta HTTP.
* *`pixelType`* pode ser usada para afetar a conversão do espaço de cores de saída quando não  `icc=` for especificada.

   O perfil de cor padrão correspondente a *`pixelType`* é aplicado. Se o gerenciamento de cores estiver desativado, a conversão ingênua será aplicada. *`pixelType`* é ignorada quando  `icc=` é especificada, o que determina o tipo de pixel de saída.

* *`compression`* é permitido somente se  `tif`,  `tif-alpha`,  `pdf`,  `webp`,  `webp-alpha`,  `jpeg2000`,  `jpeg2000-alpha`,  `jpegxr`, ou  `jpegxr-alpha` for especificado como  *`format`*. Consulte a tabela abaixo para obter as opções de compactação compatíveis com esses formatos de imagem.

Você pode usar `qlt=` para definir as opções de codificação JPEG para estes formatos: JPEG, TIFF com compactação JPEG, PDF com compactação JPEG e SWF. WebP, JPEG 2000 e JPEG XR também usam `qlt=`, mas os valores resultam em diferentes qualidades para os diferentes formatos. Use `quantize=` se `fmt=gif` ou `fmt=gif-alpha`. Consulte as descrições dos comandos para obter detalhes. Os outros formatos não têm opções configuráveis.

8 bits por componente de pixel são retornados para todos os *`formats`* e *`pixelTypes`* (8 bits por pixel para GIF).

A tabela a seguir lista as combinações válidas de *`format`*e *`pixelType`*, os tipos MIME de resposta HTTP correspondentes, se perfis ICC podem ser incorporados (consulte [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) e quais opções específicas de formato você pode aplicar.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> format</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> Tipo MIME de resposta</b> </th> 
   <th class="entry"> <b>Incorporar perfil ICC</b> </th> 
   <th class="entry"> <b> Opções</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span>,  <span class="codeph"> pscan=  </span>,  <span class="codeph"> qlt=  </span>,  <span class="codeph"> xmpEmbed=  </span> </p> <p>O parâmetro <span class="codeph"> pscan= </span> aplica-se apenas ao formato pjpeg. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alfa </p> </td> 
   <td colname="col2"> <p>rgb, cinza </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alfa </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alfa </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compressão  </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>apenas "tiff"; 'tiff-alfa' não suporta compactação jpeg. </p> <p> <span class="codeph"> qlt=  </span> </p> <p> <span class="codeph"> qlt=  </span> é ignorada, a menos que a  <span class="varname"> compactação  </span> seja definida como  <span class="codeph"> jpeg  </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alfa, swf-alfa3 </p> </td> 
   <td colname="col2"> <p>rgb, cinza </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Não </p> <p> <p>Observação:  O Flash Player Adobe ignora perfis ICC incorporados. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt=  </span>,  <span class="codeph"> atributo::TrustedDomains  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compressão  </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt=  </span> é ignorada, a menos que a  <span class="codeph"> <span class="varname"> compactação  </span> </span> seja definida como  <span class="codeph"> jpeg  </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alfa </p> </td> 
   <td colname="col2"> <p>rgb, cinza </p> <p>Os dados são convertidos em paleta após conversão em cinza ou em rgb. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td colname="col4"> <p>Não </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize=  </span> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>web, web-alfa </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>Não </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compactação  </span> </span> (  <span class="codeph"> com perda  </span>,  <span class="codeph"> sem perda  </span>) </p> <p> <span class="codeph"> qlt=  </span> é ignorado para  <span class="codeph"> sem perdas  </span>. </p> <p>Como não há conceito de redução da resolução de crominância com o formato WebP, se você usar um segundo valor com <span class="codeph"> qlt </span> (por exemplo, <span class="codeph"> qlt=80,1 </span>), o segundo valor ( <span class="codeph"> 1 </span>) será ignorado. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alfa </p> </td> 
   <td> <p>rgb, cinza </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>Não </p> </td> 
   <td> <p>O mesmo que acima. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alfa </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image&gt; </span> </p> </td> 
   <td> <p>Não </p> </td> 
   <td> <p>O mesmo que acima. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Atributo de solicitação. Aplica-se independentemente da configuração de camada atual se `req=img` (padrão) ou `req=mask`; ignorado caso contrário.

*`type`* é ignorada se  `iccProfile=` for especificada.

## Padrão {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, onde o  *`defaultType`* é tratado da seguinte forma: Se  `icc=` for especificado,  *`defaultType`* corresponde ao tipo de pixel do perfil ICC especificado. Se `icc=` não for especificado, *`defaultType`* será `gray` se `req=mask`, caso contrário será `rgb`.

## Exemplos {#section-b93222e652df404a84c69025247f07df}

**Solicite uma imagem de pré-visualização pequena e de baixa qualidade no formato JPEG (padrão):**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**Solicite a mesma imagem convertida em escala de cinza:**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Solicite a mesma imagem em um formato sem perda com canal alfa e em alta resolução:**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Solicite o canal alfa para a mesma imagem que uma imagem TIFF em escala cinza:**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Converta a mesma imagem em cmyk usando os perfis ICC padrão:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Converta a mesma imagem em cmyk usando um perfil ICC diferente e incorpore o perfil na imagem TIFF:**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Forneça esta imagem como um arquivo TIF com compactação JPEG sem conversão de tipo de pixel:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Converta a imagem em um GIF bi-tonal com transparência de cores chave e força as cores a preto e branco:**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Com perda de qualidade de 80:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Sem perdas com alfa:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Com perda de qualidade de 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Sem perdas com alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Com perda de qualidade de 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Sem perdas com alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Consulte também {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) ,  [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38),  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135)pathEmbed=, pscan.
