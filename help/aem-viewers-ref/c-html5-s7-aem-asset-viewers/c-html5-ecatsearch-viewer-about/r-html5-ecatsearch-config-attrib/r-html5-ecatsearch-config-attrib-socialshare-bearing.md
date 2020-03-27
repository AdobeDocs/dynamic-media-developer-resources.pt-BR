---
description: nulo
seo-description: nulo
seo-title: SocialShare.bear
solution: Experience Manager
title: SocialShare.bear
topic: Dynamic media
uuid: 7c64551a-71e2-4725-bf35-cbaeaaa45a40
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# SocialShare.bear{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> para cima|para baixo|para a esquerda|para a direita|vertical|lateral em forma de encaixe </span> </p> </td> 
   <td colname="col2"> <p> Especifica a direção da animação do slide para o container de botões. </p> <p> Quando definido para <span class="codeph"> cima </span>, <span class="codeph"> para baixo </span>, <span class="codeph"> para a esquerda </span>ou para a <span class="codeph"> direita </span>, o painel é lançado em uma direção especificada sem uma verificação adicional de limites. Esse comportamento pode resultar no recorte do painel por um container externo. </p> <p>Quando definido como <span class="codeph"> vertical </span>, o componente primeiro alterna a posição do painel base para a parte inferior do SocialShare e tenta implantar o painel na parte inferior, direita ou esquerda, a partir desse local base. Com cada tentativa, o componente verifica se o painel é cortado por um container externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para a parte superior e repetir as tentativas de roll-out da parte superior, direita e esquerda. </p> <p>Quando definido para <span class="codeph"> lateral, </span>o componente usa uma lógica semelhante à da vertical, mas, em vez disso, desloca a base para a direita, tentando primeiro para baixo e para cima, para baixo e para cima, para cima, para as direções de deslocamento e, em seguida, desloca a base para a esquerda, tentando para a esquerda, para baixo e para cima, para cima, para fora. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-8e843b967237426e9a8b3cd0f27b9820}

Opcional.

## Padrão {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Example {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
