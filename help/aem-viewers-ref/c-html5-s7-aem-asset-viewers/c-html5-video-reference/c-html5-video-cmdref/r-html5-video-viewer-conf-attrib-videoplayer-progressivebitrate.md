---
description: Atributo de configuração para o Visualizador de vídeo.
seo-description: Atributo de configuração para o Visualizador de vídeo.
seo-title: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
topic: Dynamic Media
uuid: 2e911d35-155e-4afa-aede-52e9d00ae211
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

Atributo de configuração para o Visualizador de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value</span> </p> </td> 
   <td colname="col2"> <p> Especifica (em kbits por segundos ou kbps) a taxa de bits de vídeo desejada para reprodução a partir de um Conjunto de vídeos adaptáveis, caso o sistema atual não suporte a reprodução de vídeo adaptável. </p> <p>O componente pega o fluxo de vídeo com a taxa de bits mais próxima (mas não superior) do valor especificado. Se todos os fluxos de vídeo no Conjunto de vídeos adaptáveis tiverem qualidade superior ao valor especificado, a lógica escolherá a taxa de bits com a qualidade mais baixa. </p> </td> 
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

