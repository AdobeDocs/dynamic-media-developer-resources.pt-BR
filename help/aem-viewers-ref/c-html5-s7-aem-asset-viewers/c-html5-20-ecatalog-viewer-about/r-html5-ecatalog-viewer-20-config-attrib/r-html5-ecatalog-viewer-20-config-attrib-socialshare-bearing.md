---
title: SocialShare.Bearing
description: SocialShare.Bearing
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026b5921-53ae-436f-bf82-dee2e699405f
TQID: 'https://experienceleague.adobe.com/sWilQyllf5wtlr-tP1kKtK4L0taRA6HWQW2Yh0MSefQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 0%

---

# SocialShare.Bearing{#socialshare-bearing}

`[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> para cima|para baixo|esquerda|direita|ajuste vertical|ajuste lateral </span> </p> </td> 
   <td colname="col2"> <p> Especifica a direção da animação do slide para o contêiner de botões. </p> <p> Quando definido como <span class="codeph"> up </span>, <span class="codeph"> down </span>, <span class="codeph"> left </span> ou <span class="codeph"> right </span>, o painel é implantado em uma direção especificada sem uma verificação de limites extras. Esse comportamento pode resultar no recorte do painel por um contêiner externo. </p> <p>Quando definido como <span class="codeph"> ajustar-vertical </span>, o componente primeiro muda a posição do painel base para a parte inferior do SocialShare e tenta implantar o painel da parte inferior, direita ou esquerda, a partir desse local base. A cada tentativa, o componente verifica se o painel é recortado por um contêiner externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para o topo e repetir as tentativas de implantação de cima, direita e esquerda. </p> <p>Quando definido como <span class="codeph"> ajuste lateral </span>, o componente usa uma lógica semelhante à do ajuste vertical. No entanto, ele desloca a base para a direita, primeiro tentando, para baixo e para cima nas direções de implantação, e então desloca a base para a esquerda, tentando para a esquerda, para baixo e para cima nas direções de implantação. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-8e843b967237426e9a8b3cd0f27b9820}

Opcional.

## Padrão {#section-da4f728f90694e3f9b4842b32c2e9952}

`fit-vertical`

## Exemplo {#section-b48f9881aca44bb5a30866d905d98035}

`bearing=left`
