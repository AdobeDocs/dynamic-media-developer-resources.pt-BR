---
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
title: VideoScrubber.chaptertimepattern
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---


# VideoScrubber.chaptertimepattern{#videoscrubber-chaptertimepattern}

Atributo de configuração para o Visualizador de vídeo interativo.

`[VideoScrubber.|<containerId>_videoScrubber.]chaptertimepattern=[h:]m|mm:s|ss`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> [h:]m|mm:s|ss</span> </p> </td> 
   <td colname="col2"> <p> Define o padrão para o tempo que é exibido na barra de título do rótulo do capítulo, onde <span class="codeph"> h</span> representa horas, <span class="codeph"> m</span> para minutos e <span class="codeph"> s</span> para segundos. </p> <p>O número de letras usadas para cada unidade de tempo determina o número de dígitos a serem exibidos para a unidade. Se o número não puder se encaixar nos dígitos fornecidos, o valor equivalente será exibido na unidade subsequente. </p> <p>Por exemplo, se a hora atual do filme for de 67 minutos e 5 segundos, um padrão de tempo de <span class="codeph"> m:ss</span> será exibido como 67:05. O mesmo tempo é exibido como 1:07:5 se o padrão de tempo for <span class="codeph"> h:mm:s</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`m:ss`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
chaptertimepattern=h:mm:ss
```

