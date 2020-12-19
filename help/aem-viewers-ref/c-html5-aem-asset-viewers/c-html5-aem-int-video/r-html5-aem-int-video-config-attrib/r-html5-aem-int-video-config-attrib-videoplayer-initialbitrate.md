---
description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-title: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
topic: Dynamic media
uuid: 251ab7d2-a0b5-4658-a2b8-6b39dd93dd5b
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Atributo de configuração para o Visualizador de vídeo interativo.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Define a taxa de bits do vídeo (em kbits por segundo ou kbps) usada para a reprodução inicial do vídeo em um desktop. </p> <p>Se esse valor de taxa de bits não existir no Conjunto de vídeos adaptáveis, o player de vídeo será start com o vídeo que tem a próxima taxa de bits mais baixa. </p> <p>Se definido como <span class="codeph"> 0</span>, o player de vídeo será start da menor taxa de bits possível. </p> <p>Aplicável somente para sistemas que não têm suporte nativo para vídeo HTML5 HLS (como navegadores Firefox, Chrome e Internet Explorer 11 no Windows 10) e quando o modo de reprodução é definido como auto. </p> </td> 
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

