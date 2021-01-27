---
description: TableOfContents.bearing
solution: Experience Manager
title: TableOfContents.bearing
topic: Dynamic Media
uuid: 791aaaa5-3777-4f68-a445-caa3d975d883
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# TableOfContents.bearing{#tableofcontents-bearing}

` [TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> lateral|vertical</span> </p> </td> 
   <td> <p> Controla a direção da aparência do painel suspenso. </p> <p>Quando definido como <span class="codeph"> fit-vertical</span>, o componente primeiro alterna a posição do painel base para a parte inferior do botão e tenta rolar o painel para a direita ou para a esquerda a partir do local base. A cada tentativa, o componente verifica se o painel está cortado por um container externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para a parte superior e repetirá as tentativas de distribuição na direção direita e esquerda. </p> <p>Quando definido como <span class="codeph"> fit-lateral</span>, o componente usa uma lógica semelhante, mas desloca a base para a direita primeiro, tentando descer e rolar para cima direções. Então, ele muda a base para a esquerda, tentando descer e rolar para cima. </p> </td> 
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

`fit-vertical,2`

## Exemplo {#section-68ff51c4e2b740c995fc5109cc0063bd}

`bearing=fit-vertical,0.5`
