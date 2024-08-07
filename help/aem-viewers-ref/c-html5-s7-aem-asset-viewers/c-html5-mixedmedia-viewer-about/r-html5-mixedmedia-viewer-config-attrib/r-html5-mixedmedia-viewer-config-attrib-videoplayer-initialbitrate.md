---
title: VideoPlayer.initialbitrate
description: VideoPlayer.initialbitrate
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a5416488-d5fe-4f55-aee4-5aedc825ac04
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`valor`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> valor </span> </span> </p> </td> 
   <td colname="col2"> <p>Define a taxa de bits de vídeo (em quilobits por segundos ou kbps) usada para a reprodução inicial de vídeo em desktops. </p> <p>Se esse valor de taxa de bits não existir no Conjunto de vídeos adaptados, o reprodutor de vídeo iniciará o vídeo com a taxa de bits mais baixa. </p> <p>Se definido como <span class="codeph"> 0 </span>, o reprodutor de vídeo começará a partir da taxa de bits mais baixa possível. Aplicável apenas para sistemas que não têm suporte nativo para vídeo HTML5 HLS (que são navegadores Firefox, Chrome e Internet Explorer 11 no Windows 10) e quando o modo de reprodução está definido como <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
