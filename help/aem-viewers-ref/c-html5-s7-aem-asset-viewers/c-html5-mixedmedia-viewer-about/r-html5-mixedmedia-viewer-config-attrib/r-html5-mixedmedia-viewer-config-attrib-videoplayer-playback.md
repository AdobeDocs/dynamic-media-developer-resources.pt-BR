---
title: VideoPlayer.playback
description: Atributo de configuração para o Visualizador de vídeo de mídia mista.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: accf2b56-d7bd-483d-9759-fa38246a0a8f
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# VideoPlayer.playback{#videoplayer-playback}

Atributo de configuração para o Visualizador de vídeo de mídia mista.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Define o tipo de reprodução usado pelo visualizador. Quando <span class="codeph"> automático</span> estiver definido, na maioria dos navegadores de desktop e em todos os dispositivos iOS, o visualizador usa o vídeo de transmissão HTML5 no formato HLS. Ele retorna à reprodução de HTML5 progressiva em determinados sistemas, como Internet Explorer e Android™ mais antigos. </p> <p>Se <span class="codeph"> progressivo</span> for especificado, o visualizador dependerá apenas da reprodução do HTML5 como suportado nativamente pelos navegadores e reproduzirá o vídeo progressivamente em todos os sistemas. </p> <p>Para obter mais informações sobre a seleção de reprodução nos modos automático e progressivo, consulte o Guia do usuário do Viewer SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
