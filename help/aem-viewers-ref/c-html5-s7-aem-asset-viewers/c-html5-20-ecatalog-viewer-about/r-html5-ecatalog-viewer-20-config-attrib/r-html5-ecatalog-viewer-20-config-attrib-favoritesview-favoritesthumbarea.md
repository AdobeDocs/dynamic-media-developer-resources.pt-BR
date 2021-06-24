---
description: FavoritesView.favoritesThumbView
solution: Experience Manager
title: FavoritesView.favoritesThumbView
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Developer,Business Practitioner
exl-id: 5c57fcc8-be67-408a-9c4c-4e15d5fe6410
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---

# FavoritesView.favoritesThumbView{#favoritesview-favoritesthumbview}

` [FavoritesView.|<containerId>_favoritesView.]favoritesThumbArea= *`area`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> area</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica a área de corte para a miniatura de Favoritos. Expressa como um valor relativo ao tamanho total do quadro, com um intervalo de <span class="codeph"> 0</span> a <span class="codeph"> 1.0</span>. </p> <p>Um valor <span class="codeph"> 1</span> significa que a imagem do quadro inteiro é usada para a miniatura. </p> <p>Um valor <span class="codeph"> 0.1</span> significa que apenas 10% do tamanho do quadro é usado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`0.1`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`favoritesThumbArea=0.5`
