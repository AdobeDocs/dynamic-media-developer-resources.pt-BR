---
title: interactivedata
description: comando URL para o Visualizador de Vídeo Interativo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# interactivedata{#interactivedata}

comando URL para o Visualizador de Vídeo Interativo.

`interactivedata= *`arquivo`*`

Os dados interativos associam determinadas regiões de tempo no conteúdo do vídeo aos dados do produto que são exibidos posteriormente nas amostras interativas ao lado do vídeo. Ele também está associado ao painel de chamada para ação exibido na conclusão da reprodução do vídeo. Ele também fornece um título para o vídeo interativo exibido no painel de chamada para ação.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> arquivo</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica uma URL ou um caminho para o conteúdo de dados interativos WebVTT. O arquivo WebVTT deve ser fornecido pelo Servidor de imagens. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

Nenhum.

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
interactivedata=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt
```
