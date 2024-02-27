---
title: fmt
description: Formato de imagem de resposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 67f8a58d-88f5-4993-9749-41a3c530adba
source-git-commit: b861d383d0a1af63ae18eb1e73231758c3352a55
workflow-type: tm+mt
source-wordcount: '1017'
ht-degree: 0%

---

# fmt{#fmt}

Formato de imagem de resposta.

`fmt=format[,` `[`*`pixelType`*`]`,`[`*`compression`*`]]`

*`format`* - avif-alpha | avif | eps | f4m | gif-alpha | gif | heic | jpeg | jpeg2000-alpha | jpeg2000 | jpegxr-alpha | jpegxr | jpg | m3u8 | pdf | pjpeg | png-alpha | png | png8-alpha | png8 | swf-alpha | swf | swf3-alpha | swf3 | tif-alpha | tif | web-alpha | webp

| *`format`* | Descrição |
|---|---|
| `avif-alpha` | AVIF com e sem perdas com canal alfa. |
| `avif` | AVIF com e sem perdas. |
| `eps` | PostScript binário encapsulado descompactado. |
| `f4m` | Formato de manifesto do Servidor de Streaming do Flash. |
| `gif-alpha` | GIF com 2 a 255 cores, além de transparência de cores-chave. |
| `gif` | GIF com 2 a 256 cores. |
| `heic` | HEIC sem perdas. Esse formato é baixado por padrão do navegador se não for compatível. |
| `jpeg` | JPEG com perda. |
| `jpeg2000-alpha` | JPEG 2000 com canal alfa sem perdas e sem perdas. |
| `jpeg2000` | JPEG 2000 com perdas e sem perdas. |
| `jpegxr-alpha` | JPEG XR com canal alfa com perda e sem perda. |
| `jpegxr` | JPEG XR com perda e sem perda. |
| `jpg` | JPG com perda. |
| `m3u8` | Formato de manifesto do Apple Streaming Server. |
| `pdf` | Imagem incorporada no PDF. |
| `pjpeg` | JPEG progressivo. |
| `png-alpha` | PNG sem perda de 24 bits com canal alfa. |
| `png` | PNG sem perda de 24 bits. |
| `png8-alpha` | PNG sem perda de 8 bits com canal alfa. |
| `png8` | PNG sem perda de 8 bits. |
| `swf-alpha` | JPEG com perda e uma máscara compactada por deflação incorporada em um arquivo swf Adobe AS2. |
| `swf` | JPEG com perda incorporado em um arquivo swf Adobe AS2. |
| `swf3-alpha` | JPEG com perda e uma máscara compactada por deflação incorporada em um arquivo swf Adobe AS3. **Nota:** os formatos swf e swf-alpha são mais adequados para os aplicativos do ActionScript 2 (Flash Player 8 e anterior). Recomenda-se o uso dos formatos swf3 e swf3-alpha para os aplicativos ActionScript3 (Flash Player 9 e posterior). |
| `swf3` | JPEG com perda incorporado em um arquivo swf Adobe AS3. |
| `tif-alpha` | TIFF com canal alfa. |
| `tif` | TIFF. |
| `webp-alpha` | WebP com e sem perdas com canal alfa. |
| `webp` | WebP com e sem perdas. |

| *`pixelType`* - rgb | cinza | cmyk |
| *`pixelType`* | Descrição |
|---|---|
| `cmyk` | Retorna dados de imagem CMYK. |
| `gray` | Retorna dados de imagem em tons de cinza. |
| `rgb` | Retorna dados da imagem de RGB. |

| *`compression`* - jpeg | com perdas | sem perda | lzw | nenhum | zip |
| *`compression`* | Descrição |
|---|---|
| `jpeg` | compactação JPEG (com perda). |
| `lossy` | compactação JPEG 2000 e JPEG XR (com perda) e WebP. |
| `lossless` | Compressão HEIC, JPEG 2000 e JPEG XR (sem perdas) e WebP. |
| `lzw` | Compressão LZW (Lempel-Ziv-Welch) (sem perdas). |
| `none` | Não compactado. |
| `zip` | Compactação &quot;Deflate&quot; (sem perda). |

* *`format`* especifica o formato de codificação de imagem para dados de imagem enviados ao cliente e o tipo MIME de resposta correspondente para o cabeçalho de resposta HTTP.
* *`pixelType`* pode ser usado para efetuar a conversão do espaço de cores de saída quando `icc=` não foi especificado.

  O perfil de cor padrão correspondente a *`pixelType`* é aplicada. Se o gerenciamento de cores estiver desativado, a conversão ingênua será aplicada. *`pixelType`* é ignorado quando `icc=` é especificado, o que determina o tipo de pixel de saída.

* *`compression`* só é permitido se `tif`, `tif-alpha`, `pdf`, `webp`, `webp-alpha`, `jpeg2000`, `jpeg2000-alpha`, `jpegxr`ou `jpegxr-alpha` é especificado como o *`format`*. Consulte a tabela abaixo para obter as opções de compactação compatíveis com esses formatos de imagem.

Você pode usar `qlt=` para definir as opções de codificação de JPEG para estes formatos: JPEG, TIFF com compactação de JPEG, PDF com compactação de JPEG e SWF. WebP, JPEG 2000 e JPEG XR também usam `qlt=` mas os valores resultam em qualidades diferentes para os diferentes formatos. Uso `quantize=` se `fmt=gif` ou `fmt=gif-alpha`. Consulte as descrições do comando para obter detalhes. Os outros formatos não têm opções que podem ser definidas.

8 bits por componente de pixel são retornados para todos *`formats`* e *`pixelTypes`* (8 bits por pixel para o GIF).

A tabela a seguir lista as combinações válidas de *`format`*e *`pixelType`*, os tipos MIME de resposta HTTP correspondentes, se os perfis ICC podem ser incorporados (consulte [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)) e quais opções específicas de formato você pode aplicar.

<table id="table_12F897A34D1D47F3AA492D4F074F09D5"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> formato</i> </b> </th> 
   <th class="entry"> <b> <i> pixelType</i> </b> </th> 
   <th class="entry"> <b> Tipo de MIME de resposta</b> </th> 
   <th class="entry"> <b>Incorporar perfil ICC</b> </th> 
   <th class="entry"> <b> Opções</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> avif, avif-alpha </p> </td> 
   <td> <p>rgb</p> </td> 
   <td> <p> <span class="codeph"> &lt;image/avif&gt; </span> </p> </td> 
   <td> <p>Não </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compactação </span> </span> ( <span class="codeph"> com perdas </span>, <span class="codeph"> sem perda </span>) </p> <p> <span class="codeph"> qlt= </span> é ignorado para <span class="codeph"> sem perda </span>. </p> <p>Como não há conceito de redução de resolução de crominância com o formato WebP, se você usar um segundo valor com <span class="codeph"> qlt </span> (por exemplo, <span class="codeph"> qlt=80,1 </span>) o segundo valor ( <span class="codeph"> 1 </span>) é ignorado. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> eps </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/eps&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> gif, gif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, cinza </p> <p>Os dados são convertidos em paleta após a conversão para cinza ou rgb. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/gif&gt; </span> </p> </td> 
   <td colname="col4"> <p>Não </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> quantize= </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> heic </p> </td> 
   <td colname="col2"> <p>rgb </p> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/heic&gt; </span> </p> </td> 
   <td colname="col4"> <p>Não </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>jpeg2000, jpeg2000-alpha </p> </td> 
   <td> <p>rgb, cinza </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/jp2&gt; </span> </p> </td> 
   <td> <p>Não </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compactação </span> </span> ( <span class="codeph"> com perdas </span>, <span class="codeph"> sem perda </span>) </p> <p> <span class="codeph"> qlt= </span> é ignorado para <span class="codeph"> sem perda </span>. </p> <p>Como não há conceito de redução de resolução de crominância com o formato WebP, se você usar um segundo valor com <span class="codeph"> qlt </span> (por exemplo, <span class="codeph"> qlt=80,1 </span>) o segundo valor ( <span class="codeph"> 1 </span>) é ignorado. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> jpeg, jpg, pjpeg </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/jpeg&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> pathEmbed= </span>, <span class="codeph"> pscan= </span>, <span class="codeph"> qlt= </span>, <span class="codeph"> xmpEmbed= </span> </p> <p>A variável <span class="codeph"> pscan= </span> se aplica somente ao formato pjpeg. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td> <p>jpegxr, jpegxr-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/vnd.ms-photo&gt; </span> </p> </td> 
   <td> <p>Não </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compactação </span> </span> ( <span class="codeph"> com perdas </span>, <span class="codeph"> sem perda </span>) </p> <p> <span class="codeph"> qlt= </span> é ignorado para <span class="codeph"> sem perda </span>. </p> <p>Como não há conceito de redução de resolução de crominância com o formato WebP, se você usar um segundo valor com <span class="codeph"> qlt </span> (por exemplo, <span class="codeph"> qlt=80,1 </span>) o segundo valor ( <span class="codeph"> 1 </span>) é ignorado. </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> pdf </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/pdf&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compactação </span> </span> <p> ( <span class="codeph"> none|zip|jpeg </span>), <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> é ignorado, a menos que <span class="codeph"> <span class="varname"> compactação </span> </span> está definida como <span class="codeph"> jpeg </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p>png8, png8-alpha </p> </td> 
   <td colname="col2"> <p>rgb </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> png, png-alpha </p> </td> 
   <td colname="col2"> <p>rgb, cinza </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/png&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> swf,swf3, swf-alpha, swf-alpha3 </p> </td> 
   <td colname="col2"> <p>rgb, cinza </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;application/x-shockwave-flash&gt; </span> </p> </td> 
   <td colname="col4"> <p>Não </p> <p> <p>Observação: o Flash Player Adobe ignora perfis ICC incorporados. </p> </p> </td> 
   <td colname="col5"> <p> <span class="codeph"> qlt= </span>, <span class="codeph"> attribute::TrustedDomains </span> </p> </td> 
  </tr>
  <tr valign="top"> 
   <td colname="col1"> <p> tif, tif-alpha </p> </td> 
   <td colname="col2"> <p>rgb, cinza, cmyk </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> &lt;image/tiff&gt; </span> </p> </td> 
   <td colname="col4"> <p>Sim </p> </td> 
   <td colname="col5"> <span class="codeph"> <span class="varname"> compactação </span> </span> <p> ( <span class="codeph"> none|lzw|zip|jpeg </span>) </p> <p>somente 'tiff'; 'tiff-alpha' não é compatível com a compactação jpeg. </p> <p> <span class="codeph"> qlt= </span> </p> <p> <span class="codeph"> qlt= </span> é ignorado, a menos que <span class="varname"> compactação </span> está definida como <span class="codeph"> jpeg </span>. </p> <p>, pathEmbed=, xmpEmbed= </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p>webp, webp-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p> <span class="codeph"> &lt;image/webp&gt; </span> </p> </td> 
   <td> <p>Não </p> </td> 
   <td> <p> <span class="codeph"> <span class="varname"> compactação </span> </span> ( <span class="codeph"> com perdas </span>, <span class="codeph"> sem perda </span>) </p> <p> <span class="codeph"> qlt= </span> é ignorado para <span class="codeph"> sem perda </span>. </p> <p>Como não há conceito de redução de resolução de crominância com o formato WebP, se você usar um segundo valor com <span class="codeph"> qlt </span> (por exemplo, <span class="codeph"> qlt=80,1 </span>) o segundo valor ( <span class="codeph"> 1 </span>) é ignorado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-5f96b0ce7c5a4df1bf52e24ea78c3dae}

Solicitar atributo. Aplica-se independentemente da configuração da camada atual se `req=img` (padrão) ou `req=mask`; ignorado caso contrário.

*`type`* é ignorado se `iccProfile=` é especificado.

## Padrão {#section-f885a785b32c44fea347db15fdb2ab1f}

` fmt=jpeg, *`defaultType`*,none`, em que o *`defaultType`* é tratado da seguinte maneira: Se `icc=` é especificado, *`defaultType`* corresponde ao tipo de pixel do perfil ICC especificado. Se `icc=` não está especificado, *`defaultType`* é `gray` se `req=mask`, caso contrário, será `rgb`.

## Exemplos {#section-b93222e652df404a84c69025247f07df}

**Solicitar uma imagem de visualização pequena e de baixa qualidade no formato JPEG (padrão):**

` http:// *`server`*/myRootId/myImageId?qlt=60&wid=200`

**Solicitar a mesma imagem convertida em escala de cinza:**

` http:// *`server`*/myRootId/myImageId?fmt=jpeg,gray&qlt=60&wid=200`

**Solicite a mesma imagem em um formato sem perdas com canal alfa e em alta resolução:**

` http:// *`server`*/myRootId/myImageId?fmt=png-alpha&wid=300`

**Solicite o canal alfa para a mesma imagem como uma imagem TIFF em tons de cinza:**

` http:// *`server`*/myRootId/myImageId?req=mask&fmt=tif,gray&wid=300`

**Converta a mesma imagem em cmyk usando os perfis ICC padrão:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,cmyk&wid=300`

**Converta a mesma imagem em cmyk usando um perfil ICC diferente e incorpore o perfil na imagem TIFF:**

` http:// *`server`*/myRootId/myImageId?fmt=tif&wid=300&icc=myPrinterProfile&iccEmbed=1`

**Entregar essa imagem como um arquivo TIF com compactação JPEG sem conversão do tipo pixel:**

` http:// *`server`*/myRootId/myImageId?fmt=tif,,jpeg&qlt=95&wid=300`

**Converta a imagem em um GIF bi-tonal com transparência de cor-chave e force as cores para preto e branco:**

` http:// *`server`*/myRootId/myImageId?fmt=gif-alpha&wid=100&quantize=adaptive,off,2,000000,ffffff`

**Com perdas e um ajuste de qualidade de 80:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp&qlt=80`

**Sem perdas com alfa:**

` http:// *`server`*/myRootId/myImageId?wid=300&fmt=webp-alpha,,lossless`

**Com perdas e um ajuste de qualidade de 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000&qlt=80`

**Sem perdas com alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpeg2000-alpha,,lossless`

**Com perdas e um ajuste de qualidade de 80:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr&qlt=80`

**Sem perdas com alfa:**

`http://server/myRootId/myImageId?wid=300&fmt=jpegxr-alpha,,lossless`

## Consulte também {#section-fce8d69c74234bf48cf814d799409541}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352) , [quantize=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-quantize.md#reference-b8069670fa474e4799ac29f0d693ca38), [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [icc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e), [pathEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pathembed.md#reference-9ccf0771d6634cf68c1c9c33cd428301), [pscan](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pscan.md#reference-b8101ed8e6c04dd28173f9597e52b135).
