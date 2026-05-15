---
title: VideoPlayer.progressivebitrate
description: VideoPlayer.progressivebitrate
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: b156d3f4-c4d3-45fe-b3d3-b7ed38f6eb4d
TQID: 'https://experienceleague.adobe.com/b-bT-L2HzXaPfnA5enf-9G3UqJkc90TqzfJYCPp-hiE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 0%

---

# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`valor`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> valor</span></span> </p> </td> 
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
