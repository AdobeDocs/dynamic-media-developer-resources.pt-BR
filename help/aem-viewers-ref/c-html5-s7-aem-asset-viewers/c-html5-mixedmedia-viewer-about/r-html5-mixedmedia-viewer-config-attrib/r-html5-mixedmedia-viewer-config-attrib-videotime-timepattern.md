---
description: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic Media
uuid: 57c86b63-7495-4f6f-bd30-8c4ebf017e36
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# VideoTime.timepattern{#videotime-timepattern}

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_9FC55144166F406DB07DFE0C57791475"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Define o padrão para o tempo que é exibido na barra de controle, em que <span class="codeph"> h</span> é horas, <span class="codeph"> m</span> é minutos e <span class="codeph"> s</span> é segundos. </p> <p>O número de letras usado para cada unidade de tempo determina o número de dígitos a serem exibidos para a unidade. Se o número não se ajustar aos dígitos indicados, o valor equivalente será exibido na unidade subsequente. </p> <p>Por exemplo, se o tempo de filme atual for de 67 minutos e 5 segundos, o padrão de tempo <span class="codeph"> m:ss</span> será exibido como 67:05. O mesmo tempo é exibido como 1:07:5 se o padrão de hora especificado for <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`m:ss`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`timepattern=h:mm:ss`
