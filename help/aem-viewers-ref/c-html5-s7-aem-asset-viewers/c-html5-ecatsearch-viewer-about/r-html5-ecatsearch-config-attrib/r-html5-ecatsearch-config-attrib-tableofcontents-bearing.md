---
description: Sumário.mancal
solution: Experience Manager
title: Sumário.mancal
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d8b88ea2-38fe-41b8-89cb-c3603c513142
TQID: 'https://experienceleague.adobe.com/LSZTGA6CTiPoNdKYO481BFXT-ApEDcF4QOf1nsh-8fo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 9cbaa81231198414806938d25961167788e93789
workflow-type: tm+mt
source-wordcount: 164
ht-degree: 0%

---

# Sumário.mancal{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> ajuste lateral|ajuste vertical</span> </p> </td> 
   <td> <p> Controla a direção da aparência do painel suspenso. </p> <p>Quando definido como <span class="codeph"> ajuste vertical</span>, o componente primeiro desloca a posição do painel base para a parte inferior de seu botão e tenta distribuir o painel para a direita ou para a esquerda a partir do local base. A cada tentativa, o componente verifica se o painel é recortado por um contêiner externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para o topo e repetir as tentativas de implantação para a direita e para a esquerda. </p> <p>Quando definido como <span class="codeph"> fit-lateral</span>, o componente usa uma lógica semelhante, mas desloca a base para a direita primeiro, tentando para baixo e para cima direções de implantação. Em seguida, ele desloca a base para a esquerda, tentando para baixo e para cima instruções de implantação. </p> </td> 
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

[!DNL `fit-vertical,2`]

## Exemplo {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]

