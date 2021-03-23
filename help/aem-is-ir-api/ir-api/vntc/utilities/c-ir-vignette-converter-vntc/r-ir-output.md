---
description: vntc gera dados de texto que são enviados para o stderr ou para o arquivo de log.
seo-description: vntc gera dados de texto que são enviados para o stderr ou para o arquivo de log.
seo-title: Saída
solution: Experience Manager
title: Saída
uuid: f2041600-408f-481c-95fc-3c112def7b8a
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 0%

---


# Saída{#output}

vntc gera dados de texto que são enviados para o stderr ou para o arquivo de log.

Os dados são formatados como uma propriedade `name=value` por registro de texto. Os valores de string não são citados. Mensagens de aviso e erro são sempre enviadas para `stderr`, mesmo se `-log` for especificado.

Certas propriedades podem ocorrer várias vezes na mesma saída. Um número de sequência, começando com 0, é anexado ao nome dessas propriedades, separado por um ponto. Essas propriedades são identificadas abaixo com um sufixo `. *`n`*` após o nome da propriedade.

As seguintes propriedades são geradas:

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>, <span class="varname"> ival</span>, <span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>A cor de fundo RGB do estilo de gabinete. Somente estilos de gabinete. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>A versão padrão do arquivo de saída. Além disso, o número de versão mais alto do arquivo que essa versão de <span class="filepath"> vntc</span> pode gerar. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">erro.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Mensagem de erro. A presença de mensagens de erro normalmente indica que nenhum arquivo de saída foi criado ou que não é adequado para uso pela Renderização de imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">arquivo.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>O caminho/nome totalmente qualificado de todos os arquivos de saída, incluindo vinhetas, arquivos de estilo de gabinete, imagens de resolução completa e imagens em miniatura. Um atributo de arquivo está presente para cada arquivo gerado (exceto o arquivo de log). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">vidro=<span class="varname"> frasco</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1, se o armário tiver portas de vidro, caso contrário, 0. Somente estilos de gabinete. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>O nome do iccProfile incorporado no <span class="varname"> sourceFile</span>. </p> <p>Vazio se <span class="varname"> sourceFile</span> não for gerenciado por cores. Apenas vinhetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">informações.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Mensagem informativa, como informações de progresso. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1 se  <span class="varname"> </span> sourceFile for uma vinheta principal, 0 se tiver sido processado anteriormente com  <span class="filepath"> </span> vnUpdateor  <span class="filepath"> vntc</span>. Apenas vinhetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">principal=<span class="varname"> Fival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> Ivalis 0 se  <span class="varname"> </span> sourceFile for um estilo de gabinete contendo dados de imagem JPEG (um aviso também é emitido nesse caso), caso contrário, 1. Gabinete e janela cobrindo somente arquivos de estilo. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>O limite máximo de memória que se aplica ao processo <span class="filepath"> vntc</span> em execução. <span class="varname"> A string </span> é  <span class="varname"> ival</span>,  <span class="varname"> ivalK</span>,  <span class="varname"> ivalM</span>,  <span class="varname"> ivalG</span> ou  <span class="codeph"> 0</span>  (desabilitada). Onde <span class="varname"> K</span>, <span class="varname"> M</span> e <span class="varname"> G</span> se referem a Kilobytes (1024 bytes), Megabytes (1048576 bytes) e Gigabytes (1073741824 bytes). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>Escala do nível de pirâmide de resolução mais baixo na vinheta de saída. Presente somente se <span class="codeph"> -pyramid</span> for especificado. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>O número de materiais salvos no <span class="varname"> sourceFile</span>. Apenas vinhetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPainéis=<span class="codeph"> Vival</span></span> </p></td> 
  <td class="stentry"> <p>O número de imagens do painel neste arquivo de estilo de gabinete. Somente estilos de gabinete. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>O número de níveis de pirâmide na vinheta de saída. Presente somente se -pirâmid for especificada. Apenas vinhetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pirâmide=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0 se a vinheta de origem ou de destino tiver uma estrutura de pirâmide. Apenas vinhetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>Para estilos de gabinete, a resolução do objeto do <span class="varname"> sourceFile</span>. Para vinhetas, essa é a resolução de material recomendada para obter resultados de renderização de melhor qualidade ao renderizar a vinheta de saída. Pixels/polegada (ppi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>A menor resolução de objeto na vinheta de saída. Apenas vinhetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>A resolução média do objeto na vinheta de saída. Apenas vinhetas. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>O caminho <span class="varname"> sourceFile</span> totalmente qualificado. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>A versão do arquivo de <span class="varname"> sourceFile</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>, <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>O tamanho do pixel da vinheta de entrada, a imagem do painel padrão em um arquivo de estilo de gabinete ou a primeira imagem de opacidade de uma janela que cobre o arquivo de estilo. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>O tipo de revestimento da janela (apenas para os estilos de cobertura): </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=sombreado ou persianas horizontais </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=persianas verticais </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=cortinas curtas de largura total </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=cortinas curtas esquerda/direita </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=cortinas de comprimento completo de largura total </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=cortinas de comprimento completo esquerda/direita </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=Cortina de café </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valor </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> </span> vntif  <span class="varname"> </span> sourceFile é uma vinheta,  <span class="codeph"> </span> vncif  <span class="varname"> </span> sourceFile é um estilo de gabinete ou  <span class="codeph"> </span> vnwif  <span class="varname"> </span> sourceFile é um estilo de cobertura de janela. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>O valor especificado com <span class="codeph"> -version</span>, ou o valor de<span class="codeph"> defaultFileVersion</span> se<span class="codeph"> -version</span> não foi especificado. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSsize=<span class="varname"> Fival</span>, <span class="varname"> Fival</span>*[, <span class="varname"> Fival</span>, <span class="varname"> Fival</span>]</span> </p></td> 
  <td class="stentry"> <p>Lista separada por vírgulas dos tamanhos de pixels de todas as exibições na vinheta de saída (a exibição de resolução completa para vinhetas de pirâmide), da imagem do painel padrão em um arquivo de estilo de gabinete ou da primeira imagem de opacidade de um arquivo de estilo de cobertura de janela. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> Ivalis 1 se o estilo do gabinete for textualizável, caso contrário, 0. Não está presente para vinhetas e arquivos de estilo de cobertura de janela. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">aviso.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>Mensagem de aviso (como quando <span class="codeph"> -imagemap</span> é especificado, mas nenhum dado de mapa é encontrado na vinheta). </p></td> 
 </tr> 
</table>

