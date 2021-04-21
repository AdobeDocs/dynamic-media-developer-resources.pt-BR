---
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
title: VideoPlayer.singleclick
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 038640c7-ae8c-43e0-979b-6010bb5e40fb
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 1%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Atributo de configuração para o Visualizador de vídeo interativo.

`[VideoPlayer.|<containerId>_videoPlayer.]singleclick=none|playPause`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|playPause</span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de clique/toque único para alternar entre reproduzir e pausar. Configurar para <span class="codeph"> nenhum</span> desativa o clique/toque único para reproduzir/pausar. Se definido como <span class="codeph"> playPause</span>, clique no vídeo para alternar entre reproduzir e pausar o vídeo. Em alguns dispositivos, você pode usar controles nativos. Nesse caso, um comportamento <span class="codeph"> singleclick</span> é desabilitado. </p> </td> 
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
