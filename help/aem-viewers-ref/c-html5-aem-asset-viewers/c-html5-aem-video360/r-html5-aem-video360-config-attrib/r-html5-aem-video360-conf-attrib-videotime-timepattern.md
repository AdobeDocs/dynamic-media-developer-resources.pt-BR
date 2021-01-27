---
description: Atributo de configuração para o visualizador Video360.
seo-description: Atributo de configuração para o visualizador Video360.
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic Media
uuid: fe145e6f-742e-44fc-b225-187a86b6700e
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# VideoTime.timepattern{#videotime-timepattern}

Atributo de configuração para o visualizador Video360.

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Define o padrão para o tempo que é exibido na barra de controle, em que <span class="codeph"> h</span> é horas, <span class="codeph"> m</span> é minutos e <span class="codeph"> s</span> é segundos. </p> <p>O número de letras usado para cada unidade de tempo determina o número de dígitos a serem exibidos para a unidade. Se o número não se ajustar aos dígitos indicados, o valor equivalente será exibido na unidade subsequente. </p> <p>Por exemplo, se o tempo de filme atual for de 67 minutos e 5 segundos, o padrão de tempo <span class="codeph"> m:ss</span> será exibido como 67:05. O mesmo tempo é exibido como 1:07:5 se o padrão de hora especificado for <span class="codeph"> h:mm:s</span>. </p> </td> 
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

