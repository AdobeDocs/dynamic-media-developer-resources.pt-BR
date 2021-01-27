---
description: Atributo de configuração para o Visualizador de vídeo.
seo-description: Atributo de configuração para o Visualizador de vídeo.
seo-title: VideoPlayer.playback
solution: Experience Manager
title: VideoPlayer.playback
topic: Dynamic Media
uuid: 5ab7a322-9de0-4a26-95be-b9b2ff8e5a84
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# VideoPlayer.playback{#videoplayer-playback}

Atributo de configuração para o Visualizador de vídeo.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Define o tipo de reprodução usado pelo visualizador. Quando <span class="codeph"> auto</span> estiver definido, na maioria dos navegadores de desktop e em todos os dispositivos iOS, o visualizador usa vídeo de fluxo contínuo HTML5 no formato HLS. Ele volta para a reprodução HTML5 progressiva em determinados sistemas, como o Internet Explorer e Android mais antigos. </p> <p>Se <span class="codeph"> progressivo</span> for especificado, o visualizador dependerá somente da reprodução HTML5, como nativamente é compatível com os navegadores, e reproduzirá vídeo progressivamente em todos os sistemas. </p> <p>Para obter mais informações sobre a seleção de reprodução nos modos automático e progressivo, consulte o Guia do usuário do SDK do visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

Ignorado quando o visualizador funciona com vídeo externo. Consulte [Suporte a vídeo externo](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```

