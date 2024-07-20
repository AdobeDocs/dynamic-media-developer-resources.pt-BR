---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: fa094d84-927b-48f2-9c82-61f2a446158b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 0%

---

# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> para cima|para baixo|esquerda|direita|ajuste vertical|ajuste lateral </span> </p> </td> 
   <td colname="col2"> <p> Especifica a direção da animação do slide para o contêiner de botões. </p> <p> Quando definido como <span class="codeph"> up </span>, <span class="codeph"> down </span>, <span class="codeph"> left </span> ou <span class="codeph"> right </span>, o painel é implantado em uma direção especificada sem uma verificação de limites adicionais. Esse comportamento pode resultar no recorte do painel por um contêiner externo. </p> <p>Quando definido como <span class="codeph"> ajustar-vertical </span>, o componente primeiro muda a posição do painel base para a parte inferior do SocialShare e tenta implantar o painel da parte inferior, direita ou esquerda, a partir desse local base. A cada tentativa, o componente verifica se o painel é recortado por um contêiner externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para o topo e repetir as tentativas de implantação nas direções superior, direita e esquerda. </p> <p>Quando definido como <span class="codeph"> ajuste lateral </span>, o componente usa uma lógica semelhante à lógica com ajuste vertical, mas, em vez disso, desloca a base para a direita na primeira tentativa, direções de implantação para baixo e para cima e, em seguida, desloca a base para a esquerda, tentando direções de implantação para baixo, para a esquerda e para cima. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-8e843b967237426e9a8b3cd0f27b9820}

Opcional.

## Padrão {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Exemplo {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
