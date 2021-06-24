---
description: Atributo de configuração para o Visualizador de vídeo.
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo
role: Developer,Business Practitioner
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 1%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Atributo de configuração para o Visualizador de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`none|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> none|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de clique/toque único para alternar entre reproduzir e pausar. Configurar para <span class="codeph"> nenhum</span> desativa o clique/toque único para reproduzir/pausar. Se definido como <span class="codeph"> playPause</span>, clicar no vídeo alterna entre a reprodução e a pausa do vídeo. Em alguns dispositivos, você pode usar controles nativos. Nesse caso, o comportamento <span class="codeph"> singleclick</span> é desativado. </p> </td> 
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
