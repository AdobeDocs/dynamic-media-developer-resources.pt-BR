---
title: VideoScrubber.chaptertimepattern
description: Atributo de configuração para o Visualizador de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: a159153a-c082-4415-9515-7b480282a31f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---

# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

Atributo de configuração para o Visualizador de vídeo.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Define o padrão para o tempo que é exibido na barra de título do rótulo do capítulo do vídeo, onde <span class="codeph"> h</span> é horas, <span class="codeph"> m</span> é minutos e <span class="codeph"> s</span> é segundos. </p> <p>O número de letras usadas para cada unidade de tempo determina o número de dígitos a serem exibidos para a unidade. Se o número não puder se encaixar nos dígitos fornecidos, o valor equivalente será exibido na unidade subsequente. </p> <p>Por exemplo, se a hora atual do filme for de 67 minutos e 5 segundos, o padrão de tempo <span class="codeph"> m:ss</span> é exibido como 67:05. O mesmo tempo é exibido como 1:07:5 se o padrão de tempo especificado for <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`m:ss`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
chaptertimepattern=h:mm:ss
```
