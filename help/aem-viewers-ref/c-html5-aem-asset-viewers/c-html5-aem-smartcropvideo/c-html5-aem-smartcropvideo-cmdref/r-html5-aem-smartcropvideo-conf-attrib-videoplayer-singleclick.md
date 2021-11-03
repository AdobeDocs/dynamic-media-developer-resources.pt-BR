---
description: Atributo de configuração para o Visualizador de vídeo de recorte inteligente.
solution: Experience Manager
title: SmartCropVideoPlayer.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 1%

---

# SmartCropVideoPlayer.singleclick{#smartcropvideoplayer-singleclick}

Atributo de configuração para o Visualizador de vídeo de recorte inteligente.

` [SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de clique/toque único para alternar entre reproduzir e pausar. Configurar como <span class="codeph"> nenhum</span> desativa o clique/toque único para reproduzir/pausar. Se estiver definido como <span class="codeph"> playPause</span>, clicar no vídeo alterna entre reproduzir e pausar o vídeo. Em alguns dispositivos, você pode usar controles nativos. Nesse caso, <span class="codeph"> singleclick</span> o comportamento está desativado. </p> </td> 
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
