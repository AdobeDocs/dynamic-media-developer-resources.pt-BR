---
description: Atributo de configuração para o visualizador Video360.
seo-description: Atributo de configuração para o visualizador Video360.
seo-title: EmbedShare.embedsizes
solution: Experience Manager
title: EmbedShare.embedsizes
topic: Dynamic Media
uuid: d3eea508-fb1e-4147-b853-a16f51725dd7
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 3%

---


# EmbedShare.embedsizes{#embedshare-embedsizes}

Atributo de configuração para o visualizador Video360.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *``*, *``*[,0|1][; *``*, *`largura/altura`*[,0|1]]`

Especifica uma lista de tamanhos incorporados para a caixa de combinação de tamanho na caixa de diálogo modal de compartilhamento incorporado.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> largura  </span> </span> </p> </td> 
   <td colname="col2"> <p> Incorporar largura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> altura  </span> </span> </p> </td> 
   <td colname="col2"> <p>Incorporar altura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Especifica se esse item de lista deve ser pré-selecionado inicialmente na caixa de combinação. </p> </td> 
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

