---
title: EmbedShare.embedsizes
description: Atributo de configuração para o Visualizador de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: cf075711-1275-4eb2-8cb6-fb2609711c7a
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 3%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

Atributo de configuração para o Visualizador de vídeo de recorte inteligente.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`largura`*, *`altura`*[,0|1][; *`largura`*, *`altura`*[,0|1]]`

Especifica uma lista de tamanhos incorporados para a caixa de combinação de tamanho na caixa de diálogo modal de compartilhamento incorporado.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> largura </span> </span> </p> </td> 
   <td colname="col2"> <p> Incorporar largura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> altura </span> </span> </p> </td> 
   <td colname="col2"> <p>Incorporar altura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Especifica se esse item de lista deve ser inicialmente pré-selecionado na caixa de combinação. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```
