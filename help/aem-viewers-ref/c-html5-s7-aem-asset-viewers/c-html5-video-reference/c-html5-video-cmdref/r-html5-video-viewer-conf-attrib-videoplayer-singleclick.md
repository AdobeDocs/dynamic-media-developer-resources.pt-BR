---
description: Atributo de configuração para o Visualizador de vídeo.
seo-description: Atributo de configuração para o Visualizador de vídeo.
seo-title: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
topic: Dynamic Media
uuid: df669b2e-31da-4de0-b480-e54402c9545c
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 1%

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

Atributo de configuração para o Visualizador de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de um clique/toque para alternar entre reproduzir/pausar. A configuração para <span class="codeph"> none</span> desativa o clique/toque único para reproduzir/pausar. Se definido como <span class="codeph"> playPause</span>, clicar no vídeo alterna entre reproduzir e pausar o vídeo. Em alguns dispositivos, você pode usar controles nativos. Nesse caso, o comportamento <span class="codeph"> singleclick</span> está desativado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`playPause`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
singleclick=none
```

