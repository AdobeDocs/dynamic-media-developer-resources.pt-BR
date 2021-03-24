---
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

Atributo de configuração para o Visualizador de vídeo interativo.

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Define a taxa de bits do vídeo (em kbits por segundo ou kbps) que é usada para a reprodução inicial do vídeo em um desktop. </p> <p>Se esse valor da taxa de bits não existir no Conjunto de vídeos adaptáveis, o reprodutor de vídeo iniciará com o vídeo que apresenta a próxima taxa de bits mais baixa. </p> <p>Se definido como <span class="codeph"> 0</span>, o reprodutor de vídeo é iniciado a partir da menor taxa de bits possível. </p> <p>Aplicável apenas para sistemas que não têm suporte nativo para vídeo HTML5 HLS (como os navegadores Firefox, Chrome e Internet Explorer 11 no Windows 10) e quando o modo de reprodução é definido como automático. </p> </td> 
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

