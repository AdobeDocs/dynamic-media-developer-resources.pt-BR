---
description: nulo
seo-description: nulo
seo-title: TabelaDeConteúdo.mancal
solution: Experience Manager
title: TabelaDeConteúdo.mancal
topic: Dynamic media
uuid: 832ebacf-d57f-4efa-ab1a-6a454f7c7a32
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# TabelaDeConteúdo.mancal{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> lateral|vertical</span> </p> </td> 
   <td> <p> Controla a direção da aparência do painel suspenso. </p> <p>Quando definido para <span class="codeph"> ajuste vertical</span>, o componente primeiro alterna a posição do painel base para a parte inferior do botão e tenta rolar o painel para a direita ou para a esquerda a partir do local base. A cada tentativa, o componente verifica se o painel está cortado por um container externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para a parte superior e repetirá as tentativas de distribuição na direção direita e esquerda. </p> <p>Quando definido para <span class="codeph"> lateral</span>, o componente usa uma lógica semelhante, mas desloca a base para a direita primeiro, tentando descer e rolar para cima em direções. Então, ele muda a base para a esquerda, tentando descer e rolar para cima. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> Define o atraso em segundos para o temporizador de ocultação automática suspenso que oculta o painel quando um usuário está ocioso. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-55436ddd78b04f538dbb9a7a8463feae}

Opcional.

## Padrão {#section-049d3f94c9794510906c6f81d6cc5485}

[!DNL `fit-vertical,2`]

## Example {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
