---
title: SmartCropVideoPlayer.playback
description: Atributo de configuração para o Visualizador de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

Atributo de configuração para o Visualizador de vídeo de recorte inteligente.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|progressivo</span> </p> </td> 
   <td colname="col2"> <p> Define o tipo de reprodução usado pelo visualizador. When <span class="codeph"> auto</span> for definido, na maioria dos navegadores de desktop e em todos os dispositivos iOS, o visualizador usará vídeo de transmissão HTML5 no formato HLS. Ele volta para a reprodução HTML5 progressiva em determinados sistemas, como o Internet Explorer e Android™ mais antigos. </p> <p>If <span class="codeph"> progressivo</span> for especificado, o visualizador dependerá apenas da reprodução do HTML5, conforme nativamente suportado pelos navegadores, e reproduzirá vídeo progressivamente em todos os sistemas. </p> <p>Para obter mais informações sobre a seleção de reprodução nos modos automático e progressivo, consulte o Guia do usuário do SDK do visualizador. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

Ignorado quando o visualizador funciona com vídeo externo. Consulte [Suporte a vídeo externo]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1f3).

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
