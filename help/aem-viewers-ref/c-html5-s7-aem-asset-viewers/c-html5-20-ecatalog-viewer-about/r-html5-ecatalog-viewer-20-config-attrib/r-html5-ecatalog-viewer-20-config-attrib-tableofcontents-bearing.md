---
title: Sumário.mancal
description: Sumário.mancal
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: b140c9ba-353d-49ef-9e6b-f5bc45e0dbfd
TQID: 'https://experienceleague.adobe.com/i8oPW8fpqvU8JaUaJ-95swaFjD6YTHcqv21s3i7-L2g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 0%

---

# Sumário.mancal{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> ajuste lateral|ajuste vertical</span> </p> </td> 
   <td> <p> Controla a direção da aparência do painel suspenso. </p> <p>Quando definido como <span class="codeph"> ajuste vertical</span>, o componente primeiro muda a posição do painel base para a parte inferior de seu botão e tenta implantar o painel para a direita ou para a esquerda do local base. A cada tentativa, o componente verifica se o painel está recortado por um contêiner externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para o topo e repetir as tentativas de implantação para a direita e para a esquerda. </p> <p>Quando definido como <span class="codeph"> fit-lateral</span>, o componente usa uma lógica semelhante, mas desloca a base para a direita primeiro, tentando direções de implantação para baixo e para cima. Em seguida, desloca a base para a esquerda, tentando para baixo e para cima direções de implantação. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname">autoHideDelay</span></span> </p> </td> 
   <td> <p> Define o atraso em segundos para o temporizador de ocultação automática suspenso que oculta o painel quando um usuário está ocioso. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-55436ddd78b04f538dbb9a7a8463feae}

Opcional.

## Padrão {#section-049d3f94c9794510906c6f81d6cc5485}

`fit-vertical,2`

## Exemplo {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
