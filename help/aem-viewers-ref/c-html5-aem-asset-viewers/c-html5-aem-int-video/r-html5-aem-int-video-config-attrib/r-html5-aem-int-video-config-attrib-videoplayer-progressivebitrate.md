---
description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-title: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
topic: Dynamic Media
uuid: 72438e50-29fc-484f-8a3b-be8909e7864f
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Atributo de configuração para o Visualizador de vídeo interativo.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Especifica em kbits por segundo (ou kbps) a taxa de bits de vídeo desejada para reproduzir de um Conjunto de vídeos adaptáveis, caso o sistema atual não suporte a reprodução de vídeo adaptável. </p> <p>O componente obtém o fluxo de vídeo com a taxa de bits mais próxima (mas não superior) do valor especificado. Se todos os fluxos de vídeo no Conjunto de vídeos adaptáveis tiverem qualidade superior ao valor especificado, a lógica escolherá a taxa de bits com a qualidade mais baixa. </p> </td> 
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

