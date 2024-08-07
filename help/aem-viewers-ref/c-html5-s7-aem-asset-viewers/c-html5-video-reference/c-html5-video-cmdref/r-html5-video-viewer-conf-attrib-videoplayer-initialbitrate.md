---
title: VideoPlayer.initialbitrate
description: Atributo de configuração para o Visualizador de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 83f2af31-e2dc-430c-b9ae-563cdcd20954
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Atributo de configuração para o Visualizador de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`valor`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> valor </span> </p> </td> 
   <td colname="col2"> <p>Define a taxa de bits de vídeo (em quilobits por segundos ou kbps) usada para a reprodução inicial de vídeo em desktops. </p> <p>Se esse valor de taxa de bits não existir no Conjunto de vídeos adaptados, o reprodutor de vídeo iniciará o vídeo com a taxa de bits mais baixa. </p> <p>Se definido como <span class="codeph"> 0 </span>, o reprodutor de vídeo começará a partir da taxa de bits mais baixa possível. Aplicável apenas para sistemas que não têm suporte nativo para vídeo HTML5 HLS (que são navegadores Firefox, Chrome e Internet Explorer 11 no Windows 10) e quando o modo de reprodução está definido como <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```
