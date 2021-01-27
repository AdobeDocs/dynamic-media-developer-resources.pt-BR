---
description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-title: VideoTime.timepattern
solution: Experience Manager
title: VideoTime.timepattern
topic: Dynamic Media
uuid: 90d36f73-44f9-4e4e-9ad6-e866749f9b2f
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# VideoTime.timepattern{#videotime-timepattern}

Atributo de configuração para o Visualizador de vídeo interativo.

`[VideoTime.|<containerId>_videoTime.]timepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Define o padrão para o tempo que é exibido na barra de controle, onde <span class="codeph"> h</span> representa horas, <span class="codeph"> m</span> para minutos e <span class="codeph"> s</span> para segundos. </p> <p>O número de letras usado para cada unidade de tempo determina o número de dígitos a serem exibidos para a unidade. Se o número não se ajustar aos dígitos indicados, o valor equivalente será exibido na unidade subsequente. </p> <p>Por exemplo, se o tempo de filme atual for de 67 minutos e 5 segundos, um padrão de tempo de <span class="codeph"> m:ss</span> será exibido como 67:05. O mesmo tempo é exibido como 1:07:5 se o padrão de hora for <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
timepattern=h:mm:ss
```

