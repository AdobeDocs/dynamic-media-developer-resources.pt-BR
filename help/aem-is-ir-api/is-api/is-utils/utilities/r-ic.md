---
description: Utilitário de conversão de imagem.
solution: Experience Manager
title: ic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 0%

---

# ic {#ic}

Utilitário de conversão de imagem.

`ic` O é uma ferramenta de linha de comando que converte arquivos de imagem para o formato de TIFF de pirâmide otimizado (PTIFF). Embora o Servidor de imagens possa processar imagens sem conversão, recomendamos que você converta todas as imagens com mais de 512x512 pixels em PTIFF. Essa conversão garante o desempenho ideal do servidor e o uso de recursos, além de minimizar os tempos de resposta.

Recomenda-se que os arquivos PTIFF com conteúdo fotográfico sejam codificados em JPEG (especifique `-jpegcompress`). O conteúdo gerado por computador pode se beneficiar da compactação sem perdas ( `-deflatecompress` ou `-lzwcompress`). A menos que seja necessária uma conversão de cores ou de tipo de pixel, os dados da imagem de origem de JPEG são transferidos para o PTIFF sem decodificação, para evitar degradação de qualidade. Nesse caso, as opções de compactação especificadas se aplicam somente aos níveis de pirâmide de resolução mais baixa.

Se você não estiver convertendo imagens grandes, não precisará definir os parâmetros que controlam quanta memória usar. No entanto, se estiver, dê `ic` mais memória usando o `-maxmem` descrita abaixo. Uma boa regra geral para calcular a quantidade de memória necessária é multiplicar a largura da imagem pela altura da imagem multiplicada pelo número de canais. Por exemplo, quatro para uma imagem de RGB com alfa vezes três. Além disso, se os canais forem de 16 bits por componente, em vez de 8, dobre o resultado final.

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
   <td colname="col2"> <p>Arquivo PTIFF de saída único (inválido se usado com SourceDirectory). </p> </td> 
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

## Devoluções {#section-36a2dcfa39824d29b69547c432366219}

0 se bem-sucedido. Se ocorrer um erro, um valor diferente de zero será retornado e os detalhes do erro serão enviados para `stderr`.

## Opções {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -descompactado </span> </p> </td> 
   <td colname="col2"> <p>Não compacte a imagem de saída. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>Usar compactação deflate (zip) (padrão). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>Use a compactação Lempel-Ziv-Welch (LZW). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>Use a codificação JPEG. Ignorado se <span class="codeph"> <span class="varname"> sourceFile </span> </span> inclui dados alfa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> qualidade </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>qualidade de JPEG (0-100; o padrão é 95). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance </span> </p> </td> 
   <td colname="col2"> <p>Desative a redução de resolução de croma JPEG (pode melhorar a qualidade do texto e dos gráficos coloridos). Isso não afeta imagens de saída CMYK ou em tons de cinza. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> quantidade </span>&gt; &lt; <span class="varname"> raio </span>&gt; &lt; <span class="varname"> limite </span>&gt; &lt; <span class="varname"> monocromático </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Aplique a máscara sem nitidez a níveis de pirâmide de subamostragem. Consulte <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> para obter detalhes. (Não aplicado à imagem com resolução total.) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>Use o caminho do clipe no arquivo de origem, se houver, para criar dados alfa associados. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Resolução de impressão (dpi) para <span class="codeph"> <span class="varname"> destFile </span> </span>; se não especificada, a resolução de impressão de <span class="codeph"> srcFile </span> é copiado para <span class="codeph"> <span class="varname"> destFile </span> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop &lt; <span class="varname"> canto </span>&gt; &lt; <span class="varname"> modo </span>&gt; &lt; <span class="varname"> tolerância </span>&gt; &lt; <span class="varname"> infoFile </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Calcule um retângulo de corte para minimizar um plano de fundo de cor sólida. Nenhuma informação de corte é gerada se o algoritmo de corte automático resultar no corte da imagem inteira. </p> <p>Para calcular o retângulo de recorte sem converter a imagem, especifique <span class="codeph"> -autocrop </span> sem <span class="codeph"> -converter </span> e sem <span class="codeph"> <span class="varname"> destFile.</span> </span></p>

<p><i><b>canto</b></i> - ul | ur | Todos | lr </p>
   <p> Especifica qual canto da imagem usar um ponto de propagação. Ignorado se o modo for 1.</p>
   <p><i><b>modo</b></i> - 0 | 1</p>
   <p>Defina como 0 para recortar com base na cor do pixel de canto especificado; funciona em dados de cor pré-multiplicados se os dados alfa estiverem associados à imagem de origem.</p>
   <p>Defina como 1 para recortar com base em dados alfa; o canto é ignorado e 0 é sempre o valor de seed; nenhum recorte é aplicado se nenhum dado alfa estiver associado à imagem de origem.</p> 
   <p><i><b>tolerância</b></i> - Tolerância de correspondência. Valor real de 0,0 a 1,0. Especifica a tolerância para valores de componentes de pixel correspondentes. Defina como 0 para correspondências exatas.</p>
   <p><i><b>infoFile</b></i> - Caminho e nome do arquivo de saída XML no qual os dados de informações de corte são gravados.</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>Copiar metadados de XMP, se disponíveis, de <span class="codeph"> <span class="varname"> sourceFile </span> </span> para <span class="codeph"> <span class="varname"> destFile </span> </span> sem modificação. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> Incorporar o perfil de cores ICC em <span class="codeph"> <span class="varname"> destFile </span> </span>, se disponível (nenhum perfil é incorporado por padrão). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> arquivo </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Caminho e nome de um arquivo de perfil ICC. Define o espaço de cores de <span class="codeph"> <span class="varname"> sourceFile </span> </span> e devem corresponder ao seu tipo de pixel. Deve ser especificado somente se nenhum perfil estiver incorporado em <span class="codeph"> <span class="varname"> sourceFile </span> </span>, pois isso substitui o perfil incorporado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> arquivo </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Caminho e nome de um arquivo de perfil ICC. Define o tipo de pixel e o espaço de cor de <span class="codeph"> <span class="varname"> destFile </span> </span>. O IC converte para este perfil se <span class="codeph"> <span class="varname"> sourceFile </span> </span> tem um perfil incorporado ou se <span class="codeph"> -imageprofile </span> também é especificado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentPerceptual </span> </p> </td> 
   <td colname="col2"> <p>Tentativa de renderização perceptiva para conversões do espaço de cores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelColorimetric </span> </p> </td> 
   <td colname="col2"> <p> Tentativa de renderização Colorimétrica relativa para conversões do espaço de cores (padrão). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsColorimetric </span> </p> </td> 
   <td colname="col2"> <p>Tentativa de renderização colorimétrica absoluta para conversões de espaço de cores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>Tentativa de renderização de saturação para conversões de espaço de cor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>Desabilitar compensação de ponto negro para determinadas conversões de cores </p> <p>Ativado por padrão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>Desativar pontilhamento (difusão de erro) ao converter cores. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> Desative a conversão automática de CMYK para RGB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>Forçar a decodificação e a recodificação de imagens de entrada de JPEG. </p> <p> <b>Atenção:</b> A aplicação desta opção pode reduzir a qualidade da imagem. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>Usar filtro de reamostragem de qualidade padrão (bi-linear). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>Usar o filtro de reamostragem (padrão) de maior qualidade (janela Lanczos). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>Use o filtro de reamostragem de qualidade superior (FlashPix). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>Reduza a resolução com o filtro de nitidez bicúbica estilo Photoshop 8x8. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage </span> </p> </td> 
   <td colname="col2"> <p> Quando especificada como a primeira opção, suprime a saída de informações de uso quando opções inválidas são encontradas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -substituir </span> </p> </td> 
   <td colname="col2"> <p>Permitir a substituição de um existente <span class="codeph"> <span class="varname"> destFile </span> </span>. Por padrão, um sufixo numérico é anexado ao nome do arquivo para impedir a substituição. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphidden </span> </p> </td> 
   <td colname="col2"> <p>Ignorar arquivos de código-fonte ocultos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>Não pare o processamento quando ocorrer um erro. Tem efeito somente ao processar vários arquivos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt; <span class="varname"> arquivo </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Caminho e nome do arquivo de log (o padrão é <span class="codeph"> stdout </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> nível </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Nível de log. </p> 
   <p>&lt; 0 - Registro desativado.</p>
   <p>0 - Lista os arquivos a serem processados.</p>
   <p>1 - Adicionar relatórios para arquivos desnecessários.</p>
   <p>2 - Adicionar relatório de progresso.</p>
   <p>3 - Adicionar relatórios sobre cada arquivo encontrado.</p>
   <p>4 - Adicionar relatórios de progresso no nível do arquivo.</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>Anexar ao arquivo de log (padrão). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>Substituir arquivo de log. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec &lt; <span class="varname"> msec </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Intervalo de log em ms para loglevel 2 e superior (o padrão é 3000). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> bytes </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Limite de uso de memória. Deve ter pelo menos 10 MB. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> por cento </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>Limite de uso de memória. O padrão é 25% da memória física. Se nenhuma delas <span class="codeph"> maxem </span> nem <span class="codeph"> maxmempercent </span> são explicitamente definidos usa o padrão maxmempercent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -version </span> </p> </td> 
   <td colname="col2"> <p> Informações de versão de retorno para este utilitário. Especifique sem nenhuma outra opção. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formatos de imagem de entrada compatíveis {#section-ab13d941d6724e65b9f84b62d949d31c}

A tabela a seguir lista os formatos de arquivo de imagem e as opções de formato compatíveis com IC.

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> Formato</b> </p> </th> 
   <th class="entry"> <p> <b> Tipo de pixel</b> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> Compactação</b> </p> </th> 
   <th class="entry"> <p> <b> Notas</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> (Bitmap do Windows) </p> </td> 
   <td> <p> RGB | indexado </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> descompactado | REGRA </p> </td> 
   <td> <p> 5/6 bits/canal indica suporte para RGB de 16 bits (5-5-5 e 5-6-5 bits/canal). </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> (Postscript Encapsulado) </p> </td> 
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
   <td> <p> Se presente, o valor de transparência na paleta é convertido em alfa. </p> </td> 
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
   <td> <p> CMYK | CMYKA | RGB | RGBA | cinza | cinzentoA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> descompactado | compactado </p> </td> 
   <td> <p> Somente imagem mesclada; camadas e canais extras são ignorados. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> REGRA </p> </td> 
   <td> <p> Somente dados de bitmap; dados de vetor são ignorados. </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA | cinza | cinzentoA | indexado </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> compactado </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA | RGB | RGBA | cinza | cinzentoA | indexado </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> descompactado | CEP | LZW | JPEG | REGRA CCITT | CCITT G3 | CCITT G4 | Bits de pacotes </p> </td> 
   <td> <p> Com exceção do primeiro canal alfa associado, os canais extras são ignorados. </p> </td> 
  </tr> 
 </tbody> 
</table>

Os perfis ICC incorporados são reconhecidos em arquivos EPS, JPG, PSD, PNG e TIFF.

Caminhos incorporados e metadados XMP são reconhecidos em arquivos EPS, JPG, PSD e TIFF.

## Exemplos {#section-3c1986b30315431989bd76b1ee5bef6d}

Converta uma única imagem com a melhor qualidade e mantenha-a na mesma pasta:

`ic -convert src/myFile.png src/myFile.tif`

Converter todas as imagens em *`srcFolder`* para TIFF de pirâmide codificada em JPEG e coloque em *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

Converter todas as imagens em *`srcFolder`*. Os dados de imagem codificados de arquivos JPG são usados para a compressão LZW de nível de resolução total e sem perdas para o restante da pirâmide de imagem dessas imagens, bem como para a imagem de saída inteira de todos os arquivos de entrada que não sejam JPG. Os tipos de pixels, perfis de cores incorporados, metadados XMP etc. são mantidos.

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
