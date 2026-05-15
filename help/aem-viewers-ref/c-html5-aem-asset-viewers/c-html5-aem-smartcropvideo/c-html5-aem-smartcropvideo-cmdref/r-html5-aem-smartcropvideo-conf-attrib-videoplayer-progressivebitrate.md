---
title: SmartCropVideoPlayer.progressivebitrate
description: Atributo de configuração para o Visualizador de Corte inteligente de vídeo.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 25e3e7e9-0979-472c-a589-aaf0e221b885
TQID: 'https://experienceleague.adobe.com/HSShyhUx64vEYIAuInb1sRH5UAdknbAkQWFjYv4yvxo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 0%

---

# SmartCropVideoPlayer.progressivebitrate{#smartcropvideoplayer-progressivebitrate}

Atributo de configuração para o Visualizador de Corte inteligente de vídeo.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]progressivebitrate= *`valor`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> valor</span> </p> </td> 
   <td colname="col2"> <p> Especifica a taxa de bits de vídeo desejada - em quilobits por segundo ou kbps - para ser reproduzida a partir de um Conjunto de vídeos adaptados caso o sistema atual não suporte a reprodução de vídeo adaptado. </p> <p>O componente captura o fluxo de vídeo com a taxa de bits mais próxima (mas sem ultrapassar) do valor especificado. Se todos os fluxos de vídeo no Conjunto de vídeos adaptados tiverem uma qualidade maior do que o valor especificado, a lógica escolherá a taxa de bits com a menor qualidade. </p> </td> 
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
