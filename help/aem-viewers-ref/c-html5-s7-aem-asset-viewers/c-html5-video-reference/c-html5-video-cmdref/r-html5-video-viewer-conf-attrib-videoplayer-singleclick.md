---
title: VideoPlayer.singleclick
description: Atributo de configuração para o Visualizador de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2fd83645-16d4-45ce-8fa8-d97dc254691f
TQID: 'https://experienceleague.adobe.com/RH1L9ADikh3LiDMwfqDdrGOZ7L08nRyFgIly2yCKZf4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 0%

---

# VideoPlayer.singleclick{#videoplayer-singleclick}

Atributo de configuração para o Visualizador de vídeo.

` [VideoPlayer.|<containerId>_videoPlayer.]singleclick= *`nenhum|playPause`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> nenhum|playPause</span> </span> </p> </td> 
   <td colname="col2"> <p> Configura o mapeamento de um clique único/toque para alternar entre reproduzir/pausar. Configurar como <span class="codeph"> nenhum</span> desabilita o clique único/toque para reproduzir/pausar. Se definido como <span class="codeph"> playPause</span>, clicar no vídeo alterna entre reproduzir e pausar o vídeo. Em alguns dispositivos, você pode usar controles nativos. Nesse caso, o comportamento <span class="codeph"> singleclick</span> está desabilitado. </p> </td> 
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
