---
title: Video360Player.initialbitrate
description: Atributo de configuração para o visualizador do Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: f36eb82a-e545-4063-8bc4-6315ed17758f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 4%

---

# Video360Player.initialbitrate{#video-player-initialbitrate}

Atributo de configuração para o visualizador do Video360.

` [Video360Player.|<containerId>_video360Player.]initialbitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Define a taxa de bits do vídeo (em kilobits por segundo ou kbps) usada para a reprodução inicial do vídeo em um desktop. </p> <p>Se esse valor da taxa de bits não existir no Conjunto de vídeos adaptáveis, o reprodutor de vídeo iniciará com o vídeo que apresenta a próxima taxa de bits mais baixa. </p> <p>Se estiver definido como <span class="codeph"> 0</span>, o reprodutor de vídeo é iniciado a partir da menor taxa de bits possível. </p> <p>Aplicável apenas para sistemas que não têm suporte nativo para vídeo HLS do HTML5 (como os navegadores Firefox, Chrome e Internet Explorer 11 no Windows 10) e quando o modo de reprodução é definido como auto. </p> </td> 
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
