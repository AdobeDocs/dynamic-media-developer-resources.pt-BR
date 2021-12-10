---
title: SocialShare.bearing
description: SocialShare.bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 0%

---

# SocialShare.bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> para cima|para baixo|para a esquerda|para a direita|para-vertical|para-caber-lateral </span> </p> </td> 
   <td colname="col2"> <p> Especifica a direção da animação de slide para o contêiner de botões. </p> <p> Quando definido como <span class="codeph"> up </span>, <span class="codeph"> down </span>, <span class="codeph"> left </span>ou <span class="codeph"> right </span>, o painel é implantado em uma direção especificada sem uma verificação de limites extra. Esse comportamento pode resultar no recorte do painel por um contêiner externo. </p> <p>Quando definido como <span class="codeph"> fit-vertical </span>, o componente primeiro alterna a posição do painel base para a parte inferior do SocialShare e tenta implantar o painel da parte inferior, direita ou esquerda, a partir desse local base. Com cada tentativa, o componente verifica se o painel está cortado por um contêiner externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para o topo e repetir as tentativas de implementação a partir da direção superior, direita e esquerda. </p> <p>Quando definido como <span class="codeph"> elementos de apoio </span>, o componente usa uma lógica semelhante à do ajuste vertical. No entanto, ele desloca a base para a direita, tentando primeiro para a direita, para baixo e para cima, para cima, para as direções - e então desloca a base para a esquerda, tentando para a esquerda, para baixo e para cima, para as direções de implementação. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-8e843b967237426e9a8b3cd0f27b9820}

Opcional.

## Padrão {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Exemplo {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
