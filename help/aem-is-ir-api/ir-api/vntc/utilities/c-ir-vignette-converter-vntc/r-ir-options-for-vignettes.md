---
description: As opções a seguir controlam o processamento de arquivos de vinheta. Eles serão ignorados se sourceFile não for uma vinheta.
seo-description: As opções a seguir controlam o processamento de arquivos de vinheta. Eles serão ignorados se sourceFile não for uma vinheta.
seo-title: Opções para vinhetas
solution: Experience Manager
title: Opções para vinhetas
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0cb40314-07ce-496b-a27b-560d7bb4fa8e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---


# Opções para vinhetas{#options-for-vignettes}

As opções a seguir controlam o processamento de arquivos de vinheta. Eles serão ignorados se sourceFile não for uma vinheta.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -content</span> </p></td> 
  <td class="stentry"> <p>Cria um arquivo XML que representa a hierarquia do objeto e inclui os atributos do objeto selecionado. O conteúdo do arquivo é o mesmo retornado pelo comando <span class="codeph"> req=content</span>. O arquivo tem o mesmo nome do arquivo de origem, mas com um sufixo <span class="filepath"> .xml</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-safar  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xywidhei</span></span> </p></td> 
  <td class="stentry"> <p>Recorte a vinheta antes de dimensionar. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> </span></span> é o canto superior esquerdo do retângulo de corte, e  <span class="codeph"><span class="varname"> com</span> largura,<span class="varname"> </span></span> é o tamanho do retângulo de corte. Os valores são coordenadas de pixel relativas à imagem de visualização de resolução total da vinheta de origem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xnynwidnhein</span></span> </p> </td> 
  <td class="stentry"> <p>Recorte a vinheta antes de dimensionar. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> </span></span> sincroniza o canto superior esquerdo do retângulo de corte e  <span class="codeph"><span class="varname"> amplia</span>,<span class="varname"> </span></span> escurece o tamanho do retângulo de corte. Os valores são normalizados em relação à imagem de visualização da vinheta de origem e devem estar entre 0.0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> widnand  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> hein não deve ser maior que 1.0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -materiais incorporados</span> </p></td> 
  <td class="stentry"> <p>Mantenha os materiais incorporados na vinheta de saída. Por padrão, os materiais são removidos da vinheta de saída. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-  <span class="varname"> frasco de altura</span></span> </p></td> 
  <td class="stentry"> <p>Uma ou mais alturas da vinheta de saída em pixels. Ignorado se -info for especificado. <span class="varname"> Pode </span> ser 0, o que indica a largura da vinheta de entrada. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escala de vinheta</a> para obter informações detalhadas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Ative a extração do arquivo de mapa de imagem da vinheta. Os dados do mapa são gravados em um arquivo HTML contendo apenas um elemento <span class="codeph"> &lt;map&gt;</span>. O arquivo de saída é nomeado como o arquivo de imagem de saída, mas com um sufixo <span class="filepath"> .htm</span>. Uma mensagem de aviso é gerada e nenhum arquivo é criado se o comando for especificado, mas nenhum dado de mapa estiver presente na vinheta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -perfil</span> </p></td> 
  <td class="stentry"> <p>Salva uma cópia do perfil ICC incorporado na vinheta em um arquivo. Uma mensagem de aviso é gerada e nenhum arquivo de perfil ICC é criado se o comando for especificado, mas nenhum perfil ICC estiver presente na vinheta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pirâmide</span> </p></td> 
  <td class="stentry"> <p>Cria uma vinheta pirâmide. Obrigatório quando imagens renderizadas devem ser exibidas com visualizadores de zoom do Dynamic Media. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escala de vinheta</a> para obter mais informações. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">- <span class="varname"> sinal de largura de miniatura</span></span> </p></td> 
  <td class="stentry"> <p>Restrição de largura e altura de pixels para a imagem em miniatura. Se especificado, uma imagem JPEG que não é maior e não maior que <span class="varname"> vírgula</span> é gerada a partir da imagem de visualização da vinheta, de uma imagem de painel do arquivo estilo gabinete ou do mapa de iluminação do primeiro estilo do arquivo de estilo de cobertura de janela. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-largura  <span class="varname"> do vídeo</span> *[,<span class="varname"> vídeo</span>]</span> </p></td> 
  <td class="stentry"> <p>Uma ou mais larguras de vinheta de saída em pixels. Ignorado se <span class="codeph"> -info</span> for especificado. <span class="varname"> Pode </span> ser 0, o que indica a altura da vinheta de entrada. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escala de vinheta</a> para obter informações detalhadas. </p></td> 
 </tr> 
</table>

