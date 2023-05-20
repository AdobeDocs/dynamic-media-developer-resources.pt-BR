---
title: VideoPlayer.progressivebitrate
description: VideoPlayer.progressivebitrate
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: b156d3f4-c4d3-45fe-b3d3-b7ed38f6eb4d
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica (em quilobits por segundo ou kbps) a taxa de bits de vídeo desejada de um Conjunto de vídeos adaptados caso o sistema atual não suporte a reprodução de vídeo adaptado. </p> <p>O componente captura o fluxo de vídeo com a taxa de bits mais próxima (mas sem ultrapassar) do valor especificado. Se todos os fluxos de vídeo no Conjunto de vídeos adaptados tiverem uma qualidade maior do que o valor especificado, a lógica escolherá a taxa de bits com a menor qualidade. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
