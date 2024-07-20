---
title: VideoPlayer.playback
description: Atributo de configuração para o Visualizador de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 54a10b30-ebf5-4f1e-aa4a-b09055453c4e
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# VideoPlayer.playback{#videoplayer-playback}

Atributo de configuração para o Visualizador de vídeo.

`[VideoPlayer.|<containerId>_videoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressive</span> </p> </td> 
   <td colname="col2"> <p> Define o tipo de reprodução usado pelo visualizador. Quando <span class="codeph"> auto</span> está definido, na maioria dos navegadores de desktop e em todos os dispositivos iOS, o visualizador usa o fluxo de vídeo HTML5 no formato HLS. Ele retorna à reprodução de HTML5 progressiva em determinados sistemas, como o Internet Explorer e o Android™ mais antigos. </p> <p>Se <span class="codeph"> progressive</span> é especificado, o visualizador depende apenas da reprodução de HTML5 como suporte nativo por navegadores e reproduz vídeo progressivamente em todos os sistemas. </p> <p>Para obter mais informações sobre a seleção de reprodução nos modos automático e progressivo, consulte o Guia do usuário do Viewer SDK. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

Ignorado quando o visualizador funciona com vídeo externo. Consulte [Suporte de Vídeo Externo](../../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/r-html5-video-viewer-20-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
