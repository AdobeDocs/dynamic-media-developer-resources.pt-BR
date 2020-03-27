---
description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-description: Atributo de configuração para o Visualizador de vídeo interativo.
seo-title: SocialShare.bear
solution: Experience Manager
title: SocialShare.bear
topic: Dynamic media
uuid: b3978280-7826-44c0-bd25-357e145121f8
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# SocialShare.bear{#socialshare-bearing}

Atributo de configuração para o Visualizador de vídeo interativo.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> para cima|para baixo|para a esquerda|para a direita|vertical|lateral em forma de encaixe</span> </p> </td> 
   <td colname="col2"> <p> Especifica a direção da animação do slide para o container de botões. Quando definido para <span class="codeph"> cima</span>, para baixo <span class="codeph"> ,</span>para a esquerda <span class="codeph"> ou para a</span>direita <span class="codeph"></span>, o painel é lançado na direção especificada sem nenhuma verificação adicional de limites, o que pode resultar no painel sendo cortado por um container externo. </p> <p>Quando definido para <span class="codeph"> ajuste vertical</span>, o componente primeiro alterna a posição do painel base para a parte inferior do SocialShare e tenta implantar o painel em uma das seguintes direções a partir desse local base: embaixo, direita, esquerda. A cada tentativa, o componente verifica se o painel é cortado por um container externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para a parte superior e repetirá as tentativas de roll-out de uma direção superior, direita e esquerda. </p> <p>Quando definido como <span class="codeph"> lateral</span>, o componente usa uma lógica semelhante, mas desloca a base para a direita primeiro, tentando direcionar para a direita, para baixo e para cima nas direções de implantação. Em seguida, desloca a base para a esquerda, tentando direcionar para a esquerda, para baixo e para cima. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## Example {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```

