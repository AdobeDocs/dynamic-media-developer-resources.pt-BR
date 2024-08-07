---
description: As opções a seguir controlam o processamento de arquivos de vinheta. Eles serão ignorados se sourceFile não for uma vinheta.
solution: Experience Manager
title: Opções de vinhetas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# Opções de vinhetas{#options-for-vignettes}

As opções a seguir controlam o processamento de arquivos de vinheta. Eles serão ignorados se sourceFile não for uma vinheta.

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -conteúdo</span> </p></td> 
  <td class="stentry"> <p>Cria um arquivo XML que representa a hierarquia de objetos e inclui os atributos de objetos selecionados. O conteúdo do arquivo é o mesmo retornado pelo comando <span class="codeph"> req=contents</span>. O arquivo tem o mesmo nome do arquivo de origem, mas com um sufixo <span class="filepath"> .xml</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-crop <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname"> hei</span></span> </p></td> 
  <td class="stentry"> <p>Recorte a vinheta antes do dimensionamento. </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> é o canto superior esquerdo do retângulo de recorte, e <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> hei</span></span> é o tamanho do retângulo de recorte. Os valores são coordenadas em pixels relativas à imagem de exibição com resolução total da vinheta de origem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widn</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>Recorte a vinheta antes do dimensionamento. </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> é o canto superior esquerdo do retângulo de recorte, e o <span class="codeph"><span class="varname"> widn</span>,<span class="varname"> hein</span></span> é o tamanho do retângulo de recorte. Os valores são normalizados em relação à imagem de exibição da vinheta de origem e devem estar entre 0.0 e 1.0. </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span> e <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span> não deve ser maior que 1,0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -materiais de incorporação</span> </p></td> 
  <td class="stentry"> <p>Manter os materiais incorporados na vinheta de saída. Por padrão, os materiais são removidos da vinheta de saída. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-altura <span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Uma ou mais alturas da vinheta de saída em pixels. Ignorado se -info for especificado. <span class="varname"> ival</span> pode ser 0, que denota a largura da vinheta de entrada. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escala de Vinheta</a> para obter informações detalhadas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>Habilite a extração do arquivo de mapa de imagem da vinheta. Os dados de mapa são gravados em um arquivo HTML que contém apenas um elemento <span class="codeph"> &lt;map&gt;</span>. O nome do arquivo de saída é igual ao do arquivo de imagem de saída, mas com um sufixo <span class="filepath"> .htm</span>. Uma mensagem de aviso é gerada e nenhum arquivo é criado se o comando for especificado, mas nenhum dado de mapa estiver presente na vinheta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> - perfil</span> </p></td> 
  <td class="stentry"> <p>Salva uma cópia do perfil ICC incorporado na vinheta em um arquivo. Uma mensagem de aviso é gerada e nenhum arquivo de perfil ICC é criado se o comando for especificado, mas nenhum perfil ICC estiver presente na vinheta. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -pirâmide</span> </p></td> 
  <td class="stentry"> <p>Cria uma vinheta em pirâmide. Obrigatório quando imagens renderizadas devem ser exibidas com visualizadores de zoom do Dynamic Media. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escala de Vinheta</a> para obter informações adicionais. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-largura de miniatura <span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Restrição de largura e altura de pixels para a imagem em miniatura. Se especificada, uma imagem de JPEG que não é mais larga nem mais alta que <span class="varname"> ival</span> é gerada a partir da imagem de exibição da vinheta, uma imagem de painel do arquivo de estilo do gabinete ou o mapa de iluminação do primeiro estilo no arquivo de estilo de revestimentos de janela. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-largura <span class="varname"> val</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Uma ou mais larguras de vinheta de saída em pixels. Ignorado se <span class="codeph"> -info</span> for especificado. <span class="varname"> ival</span> pode ser 0, que denota a altura da vinheta de entrada. Consulte <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> Escala de Vinheta</a> para obter informações detalhadas. </p></td> 
 </tr> 
</table>
