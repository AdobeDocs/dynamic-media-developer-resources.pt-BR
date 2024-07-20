---
title: FavoritesMenu.bearing
description: Especifica a direção da animação do slide para o contêiner de botões.
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

Especifica a direção da animação do slide para o contêiner de botões.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> para cima|para baixo|esquerda|direita|ajuste vertical|ajuste lateral</span> </p> </td> 
   <td colname="col2"> <p> Quando definido como <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> ou <span class="codeph"> right</span>, o painel é implantado na direção especificada sem uma verificação de limites extras, o que resulta no recorte do painel por um contêiner externo. </p> <p>Quando definido como <span class="codeph"> ajustar-vertical</span>, o componente muda primeiro a posição do painel base para a parte inferior do menu Favoritos. Ele tenta implantar o painel em uma das seguintes direções a partir desse local base: inferior, direita, esquerda. A cada tentativa, o componente verifica se o painel está recortado por um contêiner externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para o topo e repetir as tentativas de implantação de uma direção superior, direita e esquerda. </p> <p>Quando definido como <span class="codeph"> fit-lateral</span>, o componente usa uma lógica semelhante. A base é deslocada para a direita primeiro, tentando para a direita, para baixo, e para cima para implantar direções. Em seguida, desloca a base para a esquerda, tentando para a esquerda, para baixo e para cima em direção de implantação. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
