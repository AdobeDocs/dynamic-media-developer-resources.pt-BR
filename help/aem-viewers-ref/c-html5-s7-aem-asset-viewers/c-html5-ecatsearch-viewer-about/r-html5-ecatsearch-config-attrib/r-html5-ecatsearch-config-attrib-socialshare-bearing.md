---
description: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
uuid: 7c64551a-71e2-4725-bf35-cbaeaaa45a40
feature: Dynamic Media Classic,Visualizadores,SDK/API,Pesquisa de catálogo eletrônico
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---


# SocialShare.bearing{#socialshare-bearing}

[!DNL `[SocialShare.|<containerId>_socialShare.]bearing= up|down|left|right|fit-vertical|fit-lateral`]

<table id="table_0002BE81371D4E16A56FBEDD13FDF3C2"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> para cima|para baixo|para a esquerda|para a direita|para-vertical|para-caber-lateral  </span> </p> </td> 
   <td colname="col2"> <p> Especifica a direção da animação de slide para o contêiner de botões. </p> <p> Quando definido para <span class="codeph"> para cima </span>, <span class="codeph"> para baixo </span>, <span class="codeph"> para a esquerda </span> ou <span class="codeph"> para a direita </span>, o painel é implantado em uma direção especificada sem uma verificação de limites adicional. Esse comportamento pode resultar no recorte do painel por um contêiner externo. </p> <p>Quando definido como <span class="codeph"> ajuste vertical </span>, o componente primeiro alterna a posição do painel base para a parte inferior do SocialShare e tenta implantar o painel da parte inferior, direita ou esquerda, a partir desse local base. A cada tentativa, o componente verifica se o painel está cortado por um contêiner externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para a parte superior e repetir as tentativas de implantação a partir da parte superior, direita e esquerda. </p> <p>Quando definido como <span class="codeph"> fit-lateral </span>, o componente usa uma lógica semelhante à do fit-vertical, mas, em vez disso, alterna a base para a direita, tentando primeiro, para baixo e para cima, para as direções de implantação e, em seguida, alterna a base para a esquerda, tentando assim reduzir, para baixo e para cima, para as direções de implantação. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-8e843b967237426e9a8b3cd0f27b9820}

Opcional.

## Padrão {#section-da4f728f90694e3f9b4842b32c2e9952}

[!DNL `fit-vertical`]

## Exemplo {#section-b48f9881aca44bb5a30866d905d98035}

[!DNL `bearing=left`]
