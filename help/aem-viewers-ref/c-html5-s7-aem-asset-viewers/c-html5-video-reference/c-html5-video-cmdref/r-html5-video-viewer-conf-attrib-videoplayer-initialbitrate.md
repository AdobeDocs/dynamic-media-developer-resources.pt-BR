---
description: Atributo de configuração para o Visualizador de vídeo.
seo-description: Atributo de configuração para o Visualizador de vídeo.
seo-title: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
topic: Dynamic media
uuid: b2dde5f4-0449-4cad-a1f2-e336027f92c6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Atributo de configuração para o Visualizador de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>Define a taxa de bits do vídeo em kbits por segundos ou kbps que é usada para a reprodução inicial do vídeo em desktops. </p> <p>Se esse valor de taxa de bits não existir no Conjunto de vídeos adaptáveis, o player de vídeo start o vídeo com a taxa de bits mais baixa. </p> <p>Se definido como <span class="codeph"> 0, </span> os start do player de vídeo serão obtidos a partir da menor taxa de bits possível. Aplicável somente para sistemas que não têm suporte nativo para vídeo HTML5 HLS (que são navegadores Firefox, Chrome e Internet Explorer 11 no Windows 10) e quando o modo de reprodução é definido como <span class="codeph"> automático </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`1400`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
initialbitrate=600
```

