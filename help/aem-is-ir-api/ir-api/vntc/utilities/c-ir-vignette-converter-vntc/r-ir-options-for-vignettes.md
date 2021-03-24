---
description: As opções a seguir controlam o processamento de arquivos de vinheta. Eles serão ignorados se sourceFile não for uma vinheta.
solution: Experience Manager
title: Opções de vinhetas
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---


# Opções de vinhetas{#options-for-vignettes}

As opções a seguir controlam o processamento de arquivos de vinheta. Eles serão ignorados se sourceFile não for uma vinheta.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -content</span> </p></td> 
  <td class="stentry"> <p>Cria um arquivo XML que representa a hierarquia do objeto e inclui os atributos de objeto selecionados. O conteúdo do arquivo é o mesmo retornado pelo comando <span class="codeph"> req=content</span>. O arquivo tem o mesmo nome do arquivo de origem, mas com um sufixo <span class="filepath"> .xml</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cortar  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xywidhei</span></span> </p></td> 
  <td class="stentry"> <p>Recorte a vinheta antes de dimensionar. </p> <p><span class="codeph"><span class="varname"> x</span>, <span class="varname"> </span></span> é o canto superior esquerdo do retângulo de corte e  <span class="codeph"><span class="varname"> largura</span>, <span class="varname"> </span></span> é o tamanho do retângulo de corte. Os valores são coordenadas de pixel em relação à imagem de exibição de resolução completa da vinheta de origem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xnynwidnhein</span></span> </p> </td> 
  <td class="stentry"> <p>Recorte a vinheta antes de dimensionar. </p> <p><span class="codeph"><span class="varname"> xn</span>, <span class="varname"> </span></span> sincroniza o canto superior esquerdo do retângulo de corte e  <span class="codeph"><span class="varname"> alarga</span>, <span class="varname"> </span></span> escurece o tamanho do retângulo de corte. Os valores são normalizados em relação à imagem de exibição da vinheta de origem e devem estar entre 0.0...1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> widnand  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> hein não deve ser maior que 1,0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -materiais incorporados</span> </p></td> 
  <td class="stentry"> <p>Manter materiais incorporados na vinheta de saída. Por padrão, os materiais são removidos da vinheta de saída. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-  <span class="varname"> marco de altura</span></span> </p></td> 
  <td class="stentry"> <p>Uma ou mais alturas da vinheta de saída em pixels. Ignorado se -info for especificado. <span class="varname"> </span> pode ser 0, o que indica a largura da vinheta de entrada. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escalonamento de vinheta</a> para obter informações detalhadas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Habilite a extração do arquivo de mapa de imagem da vinheta. Os dados do mapa são gravados em um arquivo HTML contendo apenas um elemento <span class="codeph"> &lt;map&gt;</span> . O arquivo de saída é nomeado como o arquivo de imagem de saída, mas com um sufixo <span class="filepath"> .htm</span>. Uma mensagem de aviso é gerada e nenhum arquivo é criado se o comando for especificado, mas nenhum dado de mapa estiver presente na vinheta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -profile</span> </p></td> 
  <td class="stentry"> <p>Salva uma cópia do perfil ICC incorporado na vinheta em um arquivo. Uma mensagem de aviso é gerada e nenhum arquivo de perfil ICC é criado se o comando for especificado, mas nenhum perfil ICC estiver presente na vinheta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pirâmide</span> </p></td> 
  <td class="stentry"> <p>Cria uma vinheta pirâmide. Obrigatório quando imagens renderizadas devem ser exibidas com visualizadores de zoom do Dynamic Media. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escalonamento de vinheta</a> para obter mais informações. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Restrição de largura e altura de pixels da imagem em miniatura. Se especificado, uma imagem JPEG que não é mais ampla e não é maior que <span class="varname"> ival</span> é gerada a partir da imagem de exibição da vinheta, de uma imagem de painel do arquivo de estilo do gabinete ou do mapa de iluminação do primeiro estilo no arquivo de estilo de cobertura de janela. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-largura  <span class="varname"> do marco</span> *[, <span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Uma ou mais larguras de vinheta de saída em pixels. Ignorado se <span class="codeph"> -info</span> for especificado. <span class="varname"> </span> pode ser 0, o que indica a altura da vinheta de entrada. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escalonamento de vinheta</a> para obter informações detalhadas. </p></td> 
 </tr> 
</table>

