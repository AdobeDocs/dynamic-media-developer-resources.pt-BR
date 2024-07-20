---
title: ZoomView.iscommand
description: ZoomView.iscommand
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: faa6344a-a0b5-4b27-818b-81e9e0b721b4
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
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

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

Nenhum.

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

Quando especificado no URL do visualizador:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Quando especificado nos dados de configuração:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
