---
title: VideoPlayer.progressivebitrate
description: Atributo de configuração para o Visualizador de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 7f9f1bfe-c68f-4ad4-a4a3-e0a8952e07af
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Atributo de configuração para o Visualizador de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`valor`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> valor</span> </p> </td> 
   <td colname="col2"> <p> Especifica a taxa de bits de vídeo desejada (em quilobits por segundos ou kbps) para ser reproduzida a partir de um Conjunto de vídeos adaptados caso o sistema atual não suporte a reprodução de vídeo adaptado. </p> <p>O componente captura o fluxo de vídeo com a taxa de bits mais próxima (mas sem ultrapassar) do valor especificado. Se todos os fluxos de vídeo no Conjunto de vídeos adaptados tiverem uma qualidade maior do que o valor especificado, a lógica escolherá a taxa de bits com a menor qualidade. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`700`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
progressivebitrate=600
```
