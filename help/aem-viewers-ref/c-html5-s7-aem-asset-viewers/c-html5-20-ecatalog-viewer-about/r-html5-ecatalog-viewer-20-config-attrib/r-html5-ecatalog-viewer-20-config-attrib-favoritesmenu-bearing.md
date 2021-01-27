---
description: Especifica a direção da animação do slide para o container de botões.
seo-description: Especifica a direção da animação do slide para o container de botões.
seo-title: FavoritesMenu.bearing
solution: Experience Manager
title: FavoritesMenu.bearing
topic: Dynamic Media
uuid: badc02ef-2724-41bb-9b00-c65966be8577
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# FavoritesMenu.bearing{#favoritesmenu-bearing}

Especifica a direção da animação do slide para o container de botões.

`[FavoritesMenu.|<containerId>_favoritesMenu.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> para cima|para baixo|para a esquerda|para a direita|vertical|lateral em forma de encaixe</span> </p> </td> 
   <td colname="col2"> <p> Quando definido para <span class="codeph"> para cima</span>, <span class="codeph"> para baixo</span>, <span class="codeph"> para a esquerda</span> ou <span class="codeph"> para a direita</span>, o painel é implantado na direção especificada sem uma verificação adicional de limites, o que resulta no recorte do painel por um container externo. </p> <p>Quando definido como <span class="codeph"> fit-vertical</span>, o componente primeiro alterna a posição do painel base para a parte inferior do menu Favoritos e tenta rolar o painel em uma das seguintes direções a partir desse local base: embaixo, direita, esquerda. A cada tentativa, o componente verifica se o painel está cortado por um container externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para a parte superior e repetir as tentativas de roll-out de uma direção superior, direita e esquerda. </p> <p>Quando definido como <span class="codeph"> fit-lateral</span>, o componente usa uma lógica semelhante. A base é deslocada para a direita primeiro, tentando direita, para baixo, e para cima, em direções. Em seguida, ele desloca a base para a esquerda, tentando esquerda, para baixo e para cima rodando direções. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

`bearing=left`
