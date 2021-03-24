---
description: Utilitário de conversão de imagem.
solution: Experience Manager
title: ic
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1212'
ht-degree: 0%

---


# ic {#ic}

Utilitário de conversão de imagem.

`ic` é uma ferramenta de linha de comando que converte arquivos de imagem para o formato Pyramid TIFF (PTIFF) otimizado. Embora o Image Serving possa processar imagens sem conversão, recomendamos que você converta todas as imagens com mais de 512x512 pixels em PTIFF. Essa conversão garante o desempenho ideal do servidor e o uso de recursos e minimiza os tempos de resposta.

Recomenda-se que os arquivos PTIFF que contêm conteúdo fotográfico sejam codificados em JPEG (especifique `-jpegcompress`). O conteúdo gerado pelo computador pode se beneficiar da compactação sem perdas (`-deflatecompress` ou `-lzwcompress`). A menos que seja necessária uma conversão de cor ou de tipo pixel, os dados da imagem de origem JPEG são transferidos para o PTIFF sem decodificação, para evitar degradação de qualidade. Nesse caso, as opções de compactação especificadas se aplicam apenas aos níveis da pirâmide de resolução mais baixa.

Se você não estiver convertendo imagens grandes, não precisará definir os parâmetros que controlam a quantidade de memória a ser usada. No entanto, se estiver, forneça mais memória a `ic` usando a configuração `-maxmem` descrita abaixo. Uma boa regra para calcular a quantidade de memória necessária é multiplicar a largura da imagem por vezes a altura da imagem por vez do número de canais. Por exemplo, quatro para uma imagem RGB com alfa vezes três. Além disso, se os canais forem de 16 bits por componente, em vez de 8, duplique o resultado final.

## Uso {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>opções</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Opções de comando (veja abaixo). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>sourceFile</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>Arquivo de imagem de entrada única. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFile</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Arquivo PTIFF de saída único (não válido se usado com SourceDirectory). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Pasta contendo imagens de entrada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>destFolder</i></span> </span> </p> </td> 
   <td colname="col2"> <p>Pasta na qual os arquivos PTIFF de saída são gravados. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Retorna {#section-36a2dcfa39824d29b69547c432366219}

0 se bem-sucedido. Se ocorrer um erro, um valor diferente de zero é retornado e os detalhes do erro são enviados para `stderr`.

## Opções {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -descompactado  </span> </p> </td> 
   <td colname="col2"> <p>Não compacte a imagem de saída. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress  </span> </p> </td> 
   <td colname="col2"> <p>Use a compactação deflate (zip) (padrão). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress  </span> </p> </td> 
   <td colname="col2"> <p>Use a compactação Lempel-Ziv-Welch (LZW). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress  </span> </p> </td> 
   <td colname="col2"> <p>Use a codificação JPEG. Ignorado se <span class="codeph"> <span class="varname"> sourceFile </span> </span> incluir dados alfa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality  &lt;&gt; quality  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Qualidade JPEG (0-100; o padrão é 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsampling echrominance  </span> </p> </td> 
   <td colname="col2"> <p>Desative a redução da amostragem do croma JPEG (pode melhorar a qualidade do texto e dos gráficos de cores). Isso não tem efeito nas imagens de saída CMYK ou em tons de cinza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm  &lt;&gt; amount  </span>&gt;  &lt;&gt; radius  </span>&gt;  &lt;&gt; threshold  </span>&gt;  &lt;&gt; monochrome  </span>&gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>Aplique o mascaramento com nitidez a níveis de pirâmide subamplificados. Consulte <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> para obter detalhes. (Não aplicado à imagem de resolução completa.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath  </span> </p> </td> 
   <td colname="col2"> <p>Use o caminho do clipe no arquivo de origem, se houver, para criar dados alfa associados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi  &lt;&gt; dpi  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Resolução de impressão (dpi) para <span class="codeph"> <span class="varname"> destFile </span> </span>; se não especificado, a resolução de impressão de <span class="codeph"> srcFile </span> é copiada para <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocortar  &lt;&gt; canto  </span>&gt;  &lt;&gt; modo  </span>&gt;  &lt;&gt; tolerância  </span>&gt;  &lt;&gt; infoFile  </span>&gt;  </span><span class="varname"><span class="varname"><span class="varname"><span class="varname"> </span></span></span></span></p> </td> 
   <td colname="col2"> <p>Calcule um retângulo de corte para minimizar um plano de fundo de cor sólida. Nenhuma informação de corte será gerada se o algoritmo de corte automático resultar no corte da imagem inteira. </p> <p>Para calcular o retângulo de corte sem converter a imagem, especifique <span class="codeph"> -autorecortar </span> sem <span class="codeph"> -converter </span> e sem <span class="codeph"> <span class="varname"> destFile.</span> </span></p>

<p><i><b>corner</b></i>  - ul | ur | ll | lr </p>
   <p> Especifica qual canto da imagem usar um ponto de propagação. Ignorado se o modo for 1.</p>
   <p><i><b>modo</b></i>  - 0 | 1</p>
   <p>Defina como 0 para cortar com base na cor do pixel do canto especificado; O funciona em dados de cor pré-multiplicados se os dados alfa estiverem associados à imagem de origem.</p>
   <p>Definir como 1 para cortar com base em dados alfa; corner é ignorado e 0 é sempre o valor de seed; nenhum corte será aplicado se nenhum dado alfa estiver associado à imagem de origem.</p> 
   <p><i><b>tolerância</b></i>  - Corresponder à tolerância. Valor real de 0.0 a 1.0. Especifica a tolerância para valores de componentes de pixel correspondentes. Defina como 0 para correspondências exatas.</p>
   <p><i><b>infoFile</b></i>  - Caminho e nome do arquivo de saída XML no qual os dados de informações de corte serão gravados.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData  </span> </p> </td> 
   <td colname="col2"> <p>Copie XMP metadados, se disponíveis, de <span class="codeph"> <span class="varname"> sourceFile </span> </span> para <span class="codeph"> <span class="varname"> destFile </span> </span> sem modificação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile  </span> </p> </td> 
   <td colname="col2"> <p> Incorpore o perfil de cor ICC em <span class="codeph"> <span class="varname"> destFile </span> </span>, se disponível (nenhum perfil é incorporado por padrão). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Caminho e nome de um arquivo de perfil ICC. Define o espaço de cores de <span class="codeph"> <span class="varname"> sourceFile </span> </span> e deve corresponder ao seu tipo de pixel. Deve ser especificado somente se nenhum perfil estiver incorporado em <span class="codeph"> <span class="varname"> sourceFile </span> </span>, pois isso substitui o perfil incorporado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Caminho e nome de um arquivo de perfil ICC. Define o tipo de pixel e o espaço de cores de <span class="codeph"> <span class="varname"> destFile </span> </span>. O IC converte para esse perfil se <span class="codeph"> <span class="varname"> sourceFile </span> </span> tiver um perfil incorporado ou se <span class="codeph"> -imageprofile </span> também estiver especificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual  </span> </p> </td> 
   <td colname="col2"> <p>Propósito de renderização específico para conversões de espaço de cores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric  </span> </p> </td> 
   <td colname="col2"> <p> Propósito de renderização Colorimétrica relativa para conversões do espaço de cores (padrão). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric  </span> </p> </td> 
   <td colname="col2"> <p>Intenção de renderização Colorimétrica absoluta para conversões de espaço de cores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation  </span> </p> </td> 
   <td colname="col2"> <p>Propósito de renderização de saturação para conversões de espaço de cores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensação  </span> </p> </td> 
   <td colname="col2"> <p>Desative a compensação de pontos negros para determinadas conversões de cores </p> <p>Ativado por padrão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8  </span> </p> </td> 
   <td colname="col2"> <p>Desative o pontilhamento (difusão de erros) ao converter cores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -mainpixeltype  </span> </p> </td> 
   <td colname="col2"> <p> Desative a conversão automática de CMYK para RGB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress  </span> </p> </td> 
   <td colname="col2"> <p>Forçar decodificação e recodificação de imagens de entrada JPEG. </p> <p> <b>Cuidado:</b> aplicar essa opção pode reduzir a qualidade da imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2  </span> </p> </td> 
   <td colname="col2"> <p>Use o filtro de reamostragem de qualidade padrão (bi-linear). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8  </span> </p> </td> 
   <td colname="col2"> <p>Use o filtro de nova amostra de qualidade superior (janela Lanczos) (padrão). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix  </span> </p> </td> 
   <td colname="col2"> <p>Use o filtro de nova amostra de maior qualidade (FlashPix). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp  </span> </p> </td> 
   <td colname="col2"> <p>Reduza a amostra com o filtro Photoshop style 8x8 bicubic-shark. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage  </span> </p> </td> 
   <td colname="col2"> <p> Quando especificado como a primeira opção, suprime a saída de informações de uso quando opções inválidas são encontradas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -overwrite  </span> </p> </td> 
   <td colname="col2"> <p>Permita a substituição de um <span class="codeph"> <span class="varname"> destFile </span> </span> existente. Por padrão, um sufixo numérico é anexado ao nome do arquivo para evitar a substituição. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden  </span> </p> </td> 
   <td colname="col2"> <p>Ignorar arquivos de origem ocultos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -contínuo  </span> </p> </td> 
   <td colname="col2"> <p>Não interrompa o processamento quando ocorrer um erro. Somente tem um efeito ao processar vários arquivos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile  &lt;&gt; file  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Caminho e nome do arquivo de log (o padrão é <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel  &lt;&gt; level  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Nível de log. </p> 
   <p>&lt; 0=""&gt;</p>
   <p>0 - Lista os arquivos a serem processados.</p>
   <p>1 - Adicione relatórios para arquivos desnecessários.</p>
   <p>2 - Adicionar relatório de progresso.</p>
   <p>3 - Adicione relatórios em cada arquivo encontrado.</p>
   <p>4 - Adicionar relatório de progresso no nível do arquivo.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend  </span> </p> </td> 
   <td colname="col2"> <p>Anexar ao arquivo de log (padrão). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend  </span> </p> </td> 
   <td colname="col2"> <p>Substituir arquivo de log. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec  &lt;&gt; msec  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Intervalo de log em msec para nível de log 2 e superior (o padrão é 3000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem  &lt;&gt; bytes  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Limite de uso de memória. Deve ter pelo menos 10 MB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent  &lt;&gt; percent  </span>&gt;  </span><span class="varname"> </span></p> </td> 
   <td colname="col2"> <p>Limite de uso de memória. O padrão é 25% da memória física. Se <span class="codeph"> maxmem </span> nem <span class="codeph"> maxmempercent </span> não estiverem definidos explicitamente, o padrão maxmempercent será usado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -version  </span> </p> </td> 
   <td colname="col2"> <p> Retornar informações de versão deste utilitário. Especifique sem outras opções. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formatos de imagem de entrada suportados {#section-ab13d941d6724e65b9f84b62d949d31c}

A tabela a seguir lista os formatos de arquivo de imagem e as opções de formato compatíveis com o IC.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> Formato</b> </p> </th> 
   <th class="entry"> <p> <b> Pixel </b> <b> TypeBits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Bits/chan</b> </p> </th> 
   <th class="entry"> <p> <b> Compactação</b> </p> </th> 
   <th class="entry"> <p> <b> Notas</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Bitmap do Windows) </p> </td> 
   <td> <p> RGB | indexado </p> </td> 
   <td> <p> 3 | 5/6 | 8 </p> </td> 
   <td> <p> descompactado | RLE </p> </td> 
   <td> <p> 5/6 bits/canal indica suporte para RGB de 16 bits (5-5-5 e 5-6-5 bits/canal). </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Postscript encapsulado) </p> </td> 
   <td> <p> CMYK | RGB | cinza </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII | ASCII85 | Binário | JPEG </p> </td> 
   <td> <p> Somente os arquivos EPS gerados pelo Photoshop são compatíveis. </p> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p> CompuServe </p> <b>GIF</b> </td> 
   <td> <p> indexado </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> Se estiver presente, o valor de transparência na paleta é convertido em alfa. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK | RGB | cinza </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | cinza | cinzaA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> descompactado | comprimido </p> </td> 
   <td> <p> Somente imagem mesclada; camadas e canais extras são ignorados. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> Somente dados do bitmap; dados de vetor são ignorados. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | cinza | cinzaA | indexado </p> </td> 
   <td> <p> 3 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> compactado </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | cinza | cinzaA | indexado </p> </td> 
   <td> <p> 3 | 8 | 16 </p> </td> 
   <td> <p> descompactado | ZIP | LZW | JPEG | REGRA DE CRITÉRIO | CCITT G3 | CCITT G4 | Embalagens </p> </td> 
   <td> <p> Com exceção do primeiro canal alfa associado, canais extras são ignorados. </p> </td> 
  </tr> 
 </tbody> 
</table>

Os perfis ICC incorporados são reconhecidos nos arquivos EPS, JPG, PSD, PNG e TIFF.

Caminhos e metadados de XMP incorporados são reconhecidos em arquivos EPS, JPG, PSD e TIFF.

## Exemplos {#section-3c1986b30315431989bd76b1ee5bef6d}

Converta uma única imagem na melhor qualidade e mantenha-a na mesma pasta:

`ic -convert src/myFile.png src/myFile.tif`

Converta todas as imagens em *`srcFolder`* em TIFF de pirâmide codificados em JPEG e coloque em *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Converta todas as imagens em *`srcFolder`*. Os dados de imagem codificados de arquivos JPG são usados para a compactação LZW de nível de resolução total, sem perdas, para o restante da pirâmide de imagem dessas imagens, bem como para toda a imagem de saída de todos os arquivos de entrada não JPG. Os tipos de pixels, perfis de cores incorporados, metadados de XMP etc. são mantidas.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
