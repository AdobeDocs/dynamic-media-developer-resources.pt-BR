---
description: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
uuid: 94de31cd-2b4e-4247-b181-26666767f065
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 1%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica (em kbits por segundos ou kbps) a taxa de bits de vídeo desejada para ser reproduzido a partir de um Conjunto de Vídeo Adaptável, caso o sistema atual não ofereça suporte para reprodução de vídeo adaptável. </p> <p>O componente obtém o fluxo de vídeo com a taxa de bits mais próxima possível (mas não superior) do valor especificado. Se todos os fluxos de vídeo no Conjunto de vídeos adaptativos tiverem qualidade superior ao valor especificado, a lógica escolherá a taxa de bits com a qualidade mais baixa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
