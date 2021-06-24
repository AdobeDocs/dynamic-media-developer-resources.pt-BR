---
description: FavoritesView.maxloadradius
solution: Experience Manager
title: FavoritesView.maxloadradius
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo eletrônico
role: Developer,Business Practitioner
exl-id: 6bbf75f1-96e7-496d-9f5c-6f449f76bfdd
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 1%

---

# FavoritesView.maxloadradius{#favoritesview-maxloadradius}

` [FavoritesView.|<containerId>_favoritesView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> preloadnbr</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica o comportamento de pré-carregamento do componente. </p> <p>Quando definido como <span class="codeph"> -1</span>, todas as miniaturas são carregadas simultaneamente quando o componente é inicializado ou o ativo é alterado. </p> <p>Quando definido como <span class="codeph"> 0</span>, somente as miniaturas visíveis são carregadas. </p> <p> Quando definido como <span class="codeph"><span class="varname"> preloadnbr</span></span>, você pode especificar quantas linhas invisíveis ao redor da área visível serão pré-carregadas. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`1`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`maxloadradius=0`
