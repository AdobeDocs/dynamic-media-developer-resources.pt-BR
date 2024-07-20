---
description: o vntc gera dados de texto que são enviados para o stderr ou para o arquivo de registro.
solution: Experience Manager
title: Output
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Output{#output}

o vntc gera dados de texto que são enviados para o stderr ou para o arquivo de registro.

Os dados são formatados como uma propriedade `name=value` por registro de texto. Os valores da string não estão entre aspas. As mensagens de erro e aviso são sempre enviadas para `stderr`, mesmo se `-log` for especificado.

Certas propriedades podem ocorrer várias vezes na mesma saída. Um número de sequência, começando com 0, é anexado ao nome dessas propriedades, separadas por um ponto. Essas propriedades são identificadas abaixo com um sufixo `. *`n`*` após o nome da propriedade.

As seguintes propriedades são geradas:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>A cor do plano de fundo do RGB do estilo do gabinete. Somente estilos de gabinete. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>A versão do arquivo de saída padrão. Também é o maior número de versão de arquivo que esta versão do <span class="filepath"> vntc</span> pode gerar. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">erro.<span class="varname"> n</span>=<span class="varname"> cadeia de caracteres</span></span> </p></td> 
  <td class="stentry"> <p>Mensagem de erro. A presença de mensagens de erro geralmente indica que nenhum arquivo de saída foi criado ou que eles não são adequados para uso pela Renderização de imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">arquivo.<span class="varname"> n</span>=<span class="varname"> cadeia de caracteres</span></span> </p></td> 
  <td class="stentry"> <p>O caminho/nome totalmente qualificado de todos os arquivos de saída, incluindo vinhetas, arquivos de estilo de gabinete, imagens com resolução total e imagens em miniatura. Um atributo de arquivo está presente para cada arquivo gerado (exceto o arquivo de log). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">vidro=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> é 1 se o gabinete inclui portas de vidro; caso contrário, é 0. Somente estilos de gabinete. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> cadeia de caracteres</span></span> </p></td> 
  <td class="stentry"> <p>O nome do iccProfile incorporado no <span class="varname"> sourceFile</span>. </p> <p>Vazio se <span class="varname"> sourceFile</span> não for gerenciado por cores. Somente vinhetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">informações.<span class="varname"> n</span>=<span class="varname"> cadeia de caracteres</span></span> </p></td> 
  <td class="stentry"> <p>Mensagem informativa, como informações de progresso. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> é 1 se <span class="varname"> sourceFile</span> for uma vinheta mestra, 0 se tiver sido processada anteriormente com <span class="filepath"> vnUpdate</span> ou <span class="filepath"> vntc</span>. Somente vinhetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> é 0 se <span class="varname"> sourceFile</span> é um estilo de gabinete contendo dados de imagem JPEG (um aviso também é emitido neste caso); caso contrário, é 1. Arquivos de estilo de cobertura de gabinete e janela somente. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> cadeia de caracteres</span></span> </p></td> 
  <td class="stentry"> <p>O limite máximo de memória que se aplica ao processo <span class="filepath"> vntc</span> em execução. <span class="varname"> cadeia de caracteres</span> é <span class="varname"> ival</span>, <span class="varname"> ivalK</span>, <span class="varname"> ivalM</span>, <span class="varname"> ivalG</span> ou <span class="codeph"> 0</span> (desabilitada). Onde <span class="varname"> K</span>, <span class="varname"> M</span> e <span class="varname"> G</span> referem-se a Kilobytes (1024 bytes), Megabytes (1048576 bytes) e Gigabytes (1073741824 bytes). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Escala do nível de pirâmide de resolução mais baixa na vinheta de saída. Presente somente se <span class="codeph"> -pyramid</span> for especificado. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>O número de materiais salvos no <span class="varname"> sourceFile</span>. Somente vinhetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> val</span></span> </p></td> 
  <td class="stentry"> <p>O número de imagens do painel neste arquivo de estilo de gabinete. Somente estilos de gabinete. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> val</span></span> </p></td> 
  <td class="stentry"> <p>O número de níveis de pirâmide na vinheta de saída. Presente somente se -pyramid for especificado. Somente vinhetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pirâmide=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>0 se a vinheta de origem ou de destino tiver estrutura em pirâmide. Somente vinhetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolução=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Para estilos de gabinete, a resolução de objeto de <span class="varname"> sourceFile</span>. Para vinhetas, essa é a resolução de material recomendada para obter melhores resultados de renderização ao renderizar a vinheta de saída. Pixels/polegada (ppi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>A menor resolução de objeto na vinheta de saída. Somente vinhetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>A resolução média do objeto na vinheta de saída. Somente vinhetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> cadeia de caracteres</span></span> </p></td> 
  <td class="stentry"> <p>O caminho <span class="varname"> sourceFile</span> totalmente qualificado. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>A versão do arquivo de <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>O tamanho em pixels da vinheta de entrada, a imagem padrão do painel em um arquivo de estilo de gabinete ou a primeira imagem de opacidade de uma janela que cobre o arquivo de estilo. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>O tipo de revestimento de janela (apenas estilos de revestimento de janela): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=sombra horizontal ou persianas </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=persianas verticais </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=cortinas curtas de largura total </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=cortinas curtas esquerda/direita </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=cortinas de largura total </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=cortinas de corpo inteiro esquerda/direita </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=cortina do café </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valência </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sufixo=<span class="varname"> cadeia de caracteres</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vnt</span> se <span class="varname"> sourceFile</span> for uma vinheta, <span class="codeph"> vnc</span> se <span class="varname"> sourceFile</span> for um estilo de gabinete, ou <span class="codeph"> vnw</span> se <span class="varname"> sourceFile</span> for um estilo de cobertura de janela. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>O valor especificado com <span class="codeph"> -version</span> ou o valor de <span class="codeph"> defaultFileVersion</span> se <span class="codeph"> -version</span> não foi especificado. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>Lista separada por vírgulas dos tamanhos de pixels de todas as visualizações na vinheta de saída (a visualização de resolução total para vinhetas em pirâmide), da imagem padrão do painel em um arquivo de estilo de gabinete ou da primeira imagem de opacidade de um arquivo de estilo de cobertura de janela. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span> é 1 se o estilo de gabinete for texturável; caso contrário, é 0. Não presente para vinhetas e arquivos de estilo de revestimentos de janelas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">aviso.<span class="varname"> n</span>=<span class="varname"> cadeia de caracteres</span></span> </p></td> 
  <td class="stentry"> <p>Mensagem de aviso (como quando <span class="codeph"> -imagemap</span> é especificado, mas nenhum dado de mapa é encontrado na vinheta). </p></td> 
 </tr> 
</table>
