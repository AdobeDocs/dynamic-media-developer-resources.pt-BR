---
title: FavoritesMenu.bearing
description: Specifies the direction of slide animation for the buttons container.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: f08545fd-f039-41a1-ad0b-430ce7c1bdd1
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---

# FavoritesMenu.bearing{#favoritesmenu-bearing}

Especifica a direção da animação de slide para o contêiner de botões.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> para cima|para baixo|para a esquerda|para a direita|para-vertical|para-caber-lateral</span> </p> </td> 
   <td colname="col2"> <p> When set to <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span>, or <span class="codeph"> right</span>, the panel rolls out in specified direction without an extra bounds check, which results in panel clipping by an outside container. </p> <p>When set to <span class="codeph"> fit-vertical</span>, the component first shifts the base panel position to the bottom of the Favorites menu. It tries to roll out the panel in one of the following directions from such base location: bottom, right, left. Com cada tentativa, o componente verifica se o painel está cortado por um contêiner externo. If all attempts fail, the component tries to shift the base panel position to the top and repeat roll-out attempts from a top, right, and left direction. </p> <p>Quando definido como <span class="codeph"> elementos de apoio</span>, o componente usa uma lógica semelhante. A base é deslocada para a direita primeiro, tentando para a direita, para baixo, e para cima, em direção à esquerda. Then, it shifts the base to the left, trying left, down and up roll out directions. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Properties {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
