---
description: comando URL para Visualizador de vídeo interativo.
solution: Experience Manager
title: interativedata
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Desenvolvedor,Profissional de negócios
exl-id: f9f5aa7a-3e0a-434a-8623-b439c9b6f18b
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---

# dados interativados{#interactivedata}

comando URL para Visualizador de vídeo interativo.

`interactivedata= *`arquivo`*`

Os dados interativos associam determinadas regiões de tempo no conteúdo do vídeo aos dados do produto que são exibidos posteriormente em amostras interativas ao lado do vídeo. Ele também é associado ao painel de chamada para ação mostrado na conclusão da reprodução do vídeo. Ele também fornece um título para o vídeo interativo exibido no painel de chamada para ação.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> arquivo</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica um URL ou caminho para o conteúdo de dados interativos WebVTT. O arquivo WebVTT deve ser distribuído pelo Serviço de Imagens. </p> </td> 
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
