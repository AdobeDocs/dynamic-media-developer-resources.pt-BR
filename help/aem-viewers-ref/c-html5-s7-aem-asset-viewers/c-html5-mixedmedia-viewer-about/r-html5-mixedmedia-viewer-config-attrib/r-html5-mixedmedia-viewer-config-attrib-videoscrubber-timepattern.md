---
title: VideoScrubber.timepattern
description: VideoScrubber.timepattern
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 0536110e-a885-4fd4-baa8-742fcdba5cc9
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# VideoScrubber.timepattern{#videoscrubber-timepattern}

`[VideoScrubber.|<containerId>_videoScrubber.]timepattern=[h:]m|mm:s|ss`

<table id="table_D1D7BE09311B469983B52E34338FEAFE"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Define o padrão para o tempo que é exibido na bolha de tempo, onde <span class="codeph"> h</span> são horas, <span class="codeph"> m</span> são minutos e <span class="codeph"> s</span> são segundos. </p> <p>O número de letras usadas para cada unidade de tempo determina o número de dígitos que serão exibidos para a unidade. Se o número não couber nos dígitos fornecidos, o valor equivalente será exibido na unidade subsequente. </p> <p>Por exemplo, se a hora atual do filme for de 67 minutos e 5 segundos, o padrão de tempo <span class="codeph"> m:ss</span> será exibido como 67:05. O mesmo horário será exibido como 1:07:5 se o padrão de tempo fornecido for <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
