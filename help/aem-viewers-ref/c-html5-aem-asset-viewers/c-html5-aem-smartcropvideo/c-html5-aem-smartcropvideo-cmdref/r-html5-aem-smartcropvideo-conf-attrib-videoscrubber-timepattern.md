---
title: VideoScrubber.timepattern
description: Atributo de configuração para o Visualizador de Corte inteligente de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 4b3082f6-fb88-4c69-ab09-e24cff039222
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

Atributo de configuração para o Visualizador de Corte inteligente de vídeo.

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Define o padrão para o tempo que é exibido na bolha de tempo, onde <span class="codeph"> h</span> são horas, <span class="codeph"> m</span> são minutos e <span class="codeph"> s</span> são segundos. </p> <p>O número de letras usadas para cada unidade de tempo determina o número de dígitos que serão exibidos para a unidade. Se o número não couber nos dígitos fornecidos, o valor equivalente será exibido na unidade subsequente. </p> <p>Por exemplo, se a hora atual do filme for de 67 minutos e 5 segundos, o padrão de tempo <span class="codeph"> m:ss</span> será exibido como 67:05. O mesmo horário será exibido como 1:07:5 se o padrão de tempo fornecido for <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
timepattern=h:mm:ss
```
