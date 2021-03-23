---
description: Atributo de configuração para Visualizador de vídeo de mídia mista.
seo-description: Atributo de configuração para Visualizador de vídeo de mídia mista.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
uuid: 7016d414-aa93-4854-8f95-24e94082b5ce
feature: Dynamic Media Classic,Visualizadores,SDK/API,Conjuntos de mídias mistas
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 0%

---


# VideoPlayer.playback{#videoplayer-playback}

Atributo de configuração para Visualizador de vídeo de mídia mista.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_27B4B2DDD44D4D1CB46DD1906A92B2FD"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Define o tipo de reprodução usado pelo visualizador. Quando <span class="codeph"> auto</span> é definido, na maioria dos navegadores de desktop e em todos os dispositivos iOS, o visualizador usa vídeo de transmissão HTML5 no formato HLS. Ele volta para a reprodução HTML5 progressiva em determinados sistemas, como o Internet Explorer e Android mais antigos. </p> <p>Se <span class="codeph"> progressivo</span> for especificado, o visualizador dependerá apenas da reprodução HTML5, como nativamente compatível pelos navegadores, e reproduzirá vídeo progressivamente em todos os sistemas. </p> <p>Para obter mais informações sobre a seleção de reprodução nos modos automático e progressivo, consulte o Guia do usuário do SDK do visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-65be9301796240e38f31818229da7acc}

Opcional.

## Padrão {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`auto`

## Exemplo {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`playback=progressive`
