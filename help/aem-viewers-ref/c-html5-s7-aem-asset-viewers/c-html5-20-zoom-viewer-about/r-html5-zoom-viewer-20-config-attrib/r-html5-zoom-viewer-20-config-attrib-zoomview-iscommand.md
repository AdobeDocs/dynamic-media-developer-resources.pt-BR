---
title: ZoomView.iscommand
description: ZoomView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: bab0a648-a365-4df1-bded-ba0202e62e1f
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 0%

---

# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname">iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> A sequência de comando do Servidor de imagens que é aplicada à imagem com zoom. Se especificado no URL, todas as ocorrências de <span class="codeph"> &amp;</span> e <span class="codeph"> =</span> devem ser codificadas em HTTP como <span class="codeph"> %26</span> e <span class="codeph"> %3D</span>, respectivamente. </p> <p> <p>Observação: não há suporte para comandos de manipulação de dimensionamento de imagem. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

Nenhum.

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

Quando especificado no URL do visualizador:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Quando especificado nos dados de configuração:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
