---
title: SmartCropVideoPlayer.playback
description: Atributo de configuração para o Visualizador de Corte inteligente de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 6df94fe7-30ea-42f1-a39e-50219259a098
source-git-commit: 8c49595fe0efb684b59601fb268bd8bf97fae555
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# SmartCropVideoPlayer.playback{#smartcropvideoplayer-playback}

Atributo de configuração para o Visualizador de Corte inteligente de vídeo.

`[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]playback=auto|progressive`

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

Ignorado quando o visualizador funciona com vídeo externo. Consulte [Suporte de Vídeo Externo]
(../../../c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/r-html5-aem-smartcropvideo-viewer-external-video-support.md#concept-22c67fee43274a29b28ee16770b1b1f3).

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`auto`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
playback=progressive
```
