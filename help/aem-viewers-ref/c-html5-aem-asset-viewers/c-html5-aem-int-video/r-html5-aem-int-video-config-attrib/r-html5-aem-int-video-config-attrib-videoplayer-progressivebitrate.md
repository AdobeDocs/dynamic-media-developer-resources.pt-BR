---
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
title: VideoPlayer.progressivebitrate
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Developer,Business Practitioner
exl-id: 69f3c4c0-00d9-46ef-aebb-3116a0d83c85
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Atributo de configuração para o Visualizador de vídeo interativo.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Especifica em kbits por segundo (ou kbps), a taxa de bits de vídeo desejada para ser reproduzida a partir de um Conjunto de Vídeo Adaptável, caso o sistema atual não ofereça suporte para reprodução de vídeo adaptável. </p> <p>O componente obtém o fluxo de vídeo com a taxa de bits mais próxima possível (mas não superior) do valor especificado. Se todos os fluxos de vídeo no Conjunto de vídeos adaptativos tiverem qualidade superior ao valor especificado, a lógica escolherá a taxa de bits com a qualidade mais baixa. </p> </td> 
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
