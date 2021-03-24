---
description: VideoPlayer.initialbitrate
solution: Experience Manager
title: VideoPlayer.initialbitrate
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 0%

---


# VideoPlayer.initialbitrate{#videoplayer-initialbitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]initialbitrate= *`value`*`

<table id="table_6B56976AEADA440A9A6BC9C4F65D4ADA"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
   <td colname="col2"> <p>Define a taxa de bits do vídeo em kbits por segundo ou kbps-que é usada para a reprodução inicial do vídeo em desktops. </p> <p>Se esse valor da taxa de bits não existir no Conjunto de vídeos adaptáveis, o reprodutor de vídeo iniciará o vídeo com a próxima taxa de bits mais baixa. </p> <p>Se definido como <span class="codeph"> 0 </span>, o reprodutor de vídeo é iniciado a partir da menor taxa de bits possível. Aplicável apenas para sistemas que não têm suporte nativo para vídeo HTML5 HLS (que são navegadores Firefox, Chrome e Internet Explorer 11 no Windows 10) e quando o modo de reprodução é definido como <span class="codeph"> auto </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1400`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`initialbitrate=600`
