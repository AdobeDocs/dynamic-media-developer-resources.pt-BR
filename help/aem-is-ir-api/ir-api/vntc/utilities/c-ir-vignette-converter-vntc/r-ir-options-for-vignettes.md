---
description: As opções a seguir controlam o processamento de arquivos de vinheta. Eles serão ignorados se sourceFile não for uma vinheta.
seo-description: As opções a seguir controlam o processamento de arquivos de vinheta. Eles serão ignorados se sourceFile não for uma vinheta.
seo-title: Opções para vinhetas
solution: Experience Manager
title: Opções para vinhetas
topic: Scene7 Image Serving - Image Rendering API
uuid: 0cb40314-07ce-496b-a27b-560d7bb4fa8e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Opções para vinhetas{#options-for-vignettes}

As opções a seguir controlam o processamento de arquivos de vinheta. Eles serão ignorados se sourceFile não for uma vinheta.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -content</span> </p></td> 
  <td class="stentry"> <p>Cria um arquivo XML que representa a hierarquia do objeto e inclui os atributos do objeto selecionado. O conteúdo do arquivo é o mesmo retornado pelo comando <span class="codeph"> req=content</span> . O arquivo tem o mesmo nome do arquivo de origem, mas com um sufixo <span class="filepath"> .xml</span> . </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-safra <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>Recorte a vinheta antes de dimensionar. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> é o canto superior esquerdo do retângulo de cultura e <span class="codeph"><span class="varname"> o tamanho do retângulo de cultura é o da largura</span>,<span class="varname"> hei</span></span> . Os valores são coordenadas de pixel relativas à imagem de visualização de resolução total da vinheta de origem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widescreen</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>Recorte a vinheta antes de dimensionar. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> é o canto superior esquerdo do retângulo de corte, e o <span class="codeph"><span class="varname"> widn</span>,<span class="varname"> hein</span></span> é o tamanho do retângulo de corte. Os valores são normalizados em relação à imagem de visualização da vinheta de origem e devem estar entre 0.0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span> e <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span> não devem ser maiores que 1.0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -materiais incorporados</span> </p></td> 
  <td class="stentry"> <p>Mantenha os materiais incorporados na vinheta de saída. Por padrão, os materiais são removidos da vinheta de saída. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">Frasco para injetáveis de altura <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>Uma ou mais alturas da vinheta de saída em pixels. Ignorado se -info for especificado. <span class="varname"> o valor do campo</span> pode ser 0, o que indica a largura da vinheta de entrada. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escala</a> de vinheta para obter informações detalhadas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Ative a extração do arquivo de mapa de imagem da vinheta. Os dados do mapa são gravados em um arquivo HTML contendo apenas um elemento <span class="codeph"> &lt;map&gt;</span> . O arquivo de saída é nomeado como o arquivo de imagem de saída, mas com um sufixo <span class="filepath"> .htm</span> . Uma mensagem de aviso é gerada e nenhum arquivo é criado se o comando for especificado, mas nenhum dado de mapa estiver presente na vinheta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -perfil</span> </p></td> 
  <td class="stentry"> <p>Salva uma cópia do perfil ICC incorporado na vinheta em um arquivo. Uma mensagem de aviso é gerada e nenhum arquivo de perfil ICC é criado se o comando for especificado, mas nenhum perfil ICC estiver presente na vinheta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pirâmide</span> </p></td> 
  <td class="stentry"> <p>Cria uma vinheta pirâmide. Obrigatório quando as imagens renderizadas devem ser exibidas com visualizadores de zoom do Scene7. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escala</a> de vinheta para obter mais informações. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-minilargura <span class="varname"> do vídeo</span></span> </p></td> 
  <td class="stentry"> <p>Restrição de largura e altura de pixels para a imagem em miniatura. Se especificado, uma imagem JPEG que não é mais larga e não é maior do que o <span class="varname"> vídeo</span> é gerada a partir da imagem da visualização da vinheta, de uma imagem do painel do arquivo estilo gabinete ou do mapa de iluminação do primeiro estilo do arquivo de estilo de cobertura da janela. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-largura <span class="varname"> do campo</span> *[,<span class="varname"> campo</span>]</span> </p></td> 
  <td class="stentry"> <p>Uma ou mais larguras de vinheta de saída em pixels. Ignorado se <span class="codeph"> -info</span> for especificado. <span class="varname"> o frasco para injetáveis</span> pode ser 0, o que indica a altura da vinheta de entrada. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escala</a> de vinheta para obter informações detalhadas. </p></td> 
 </tr> 
</table>

