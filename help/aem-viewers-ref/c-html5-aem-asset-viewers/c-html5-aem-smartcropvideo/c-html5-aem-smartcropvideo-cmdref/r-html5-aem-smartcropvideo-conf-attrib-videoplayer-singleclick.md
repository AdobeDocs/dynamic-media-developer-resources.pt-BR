---
title: SmartCropVideoPlayer.singleclick
description: Atributo de configuração para o Visualizador de Corte inteligente de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: f48f0866-4eb7-46c5-a7f5-457df7a568e7
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---

# SmartCropVideoPlayer.singleclick{#smartcropvideoplayer-singleclick}

Atributo de configuração para o Visualizador de Corte inteligente de vídeo.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de um clique único/toque para alternar entre reproduzir/pausar. Configuração para <span class="codeph"> nenhum</span> desativa o clique único/toque para reproduzir/pausar. Se definida como <span class="codeph"> playPause</span>, ao clicar no vídeo, ocorre a alternância entre a reprodução e a pausa do vídeo. Em alguns dispositivos, você pode usar controles nativos. Nesse caso, <span class="codeph"> singleclick</span> O comportamento do está desativado. </p> </td> 
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
