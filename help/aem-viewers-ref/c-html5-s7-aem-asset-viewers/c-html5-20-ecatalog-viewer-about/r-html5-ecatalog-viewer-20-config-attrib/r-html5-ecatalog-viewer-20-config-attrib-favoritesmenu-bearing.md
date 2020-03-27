---
description: Especifica a direção da animação do slide para o container de botões.
seo-description: Especifica a direção da animação do slide para o container de botões.
seo-title: FavoritesMenu.bear
solution: Experience Manager
title: FavoritesMenu.bear
topic: Dynamic media
uuid: badc02ef-2724-41bb-9b00-c65966be8577
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FavoritesMenu.bear{#favoritesmenu-bearing}

Especifica a direção da animação do slide para o container de botões.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> para cima|para baixo|para a esquerda|para a direita|vertical|lateral em forma de encaixe</span> </p> </td> 
   <td colname="col2"> <p> Quando definido para <span class="codeph"> cima</span>, <span class="codeph"> baixo</span>, <span class="codeph"> esquerda</span>ou <span class="codeph"> direita</span>, o painel é lançado na direção especificada sem uma verificação adicional de limites, resultando no recorte do painel por um container externo. </p> <p>Quando definido para <span class="codeph"> ajuste vertical</span>, o componente primeiro alterna a posição do painel base para a parte inferior do menu Favoritos e tenta rolar o painel em uma das seguintes direções a partir desse local base: embaixo, direita, esquerda. A cada tentativa, o componente verifica se o painel está cortado por um container externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para a parte superior e repetir as tentativas de roll-out de uma direção superior, direita e esquerda. </p> <p>Quando definido para <span class="codeph"> lateral</span>, o componente usa uma lógica semelhante. A base é deslocada para a direita primeiro, tentando direita, para baixo, e para cima, em direções. Em seguida, ele desloca a base para a esquerda, tentando esquerda, para baixo e para cima rodando direções. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
