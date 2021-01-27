---
description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-title: VideoPlayer.singleclick
solution: Experience Manager
title: VideoPlayer.singleclick
topic: Dynamic Media
uuid: 5b387eb6-1e09-4506-beea-3f1cf337cb9d
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 1%

---


# VideoPlayer.singleclick{#videoplayer-singleclick}

Atributo de configuração para o Visualizador de vídeo interativo.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de um clique/toque para alternar entre reproduzir/pausar. A configuração para <span class="codeph"> none</span> desativa o clique/toque único para reproduzir/pausar. Se definido como <span class="codeph"> playPause</span>, clicar no vídeo alterna entre reproduzir e pausar o vídeo. Em alguns dispositivos, você pode usar controles nativos. Nesse caso, um comportamento <span class="codeph"> singleclick</span> está desativado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`playPause`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
singleclick=none
```

