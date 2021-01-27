---
description: VideoPlayer.progressivebitrate
solution: Experience Manager
title: VideoPlayer.progressivebitrate
topic: Dynamic Media
uuid: 94de31cd-2b4e-4247-b181-26666767f065
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---


# VideoPlayer.progressivebitrate{#videoplayer-progressivebitrate}

` [VideoPlayer.|<containerId>_videoPlayer.]progressivebitrate= *`value`*`

<table id="table_678AFC7BC06F41188F820502D2014C1F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> value</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica (em kbits por segundos ou kbps) a taxa de bits de vídeo desejada para reprodução a partir de um Conjunto de vídeos adaptáveis, caso o sistema atual não suporte a reprodução de vídeo adaptável. </p> <p>O componente pega o fluxo de vídeo com a taxa de bits mais próxima (mas não superior) do valor especificado. Se todos os fluxos de vídeo no Conjunto de vídeos adaptáveis tiverem qualidade superior ao valor especificado, a lógica escolherá a taxa de bits com a qualidade mais baixa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`700`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`progressivebitrate=600`
