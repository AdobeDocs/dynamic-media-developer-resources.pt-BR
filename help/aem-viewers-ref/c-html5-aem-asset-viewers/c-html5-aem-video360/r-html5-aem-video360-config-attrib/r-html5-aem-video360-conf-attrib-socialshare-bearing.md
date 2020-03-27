---
description: Atributo de configuração para o visualizador do Video360.
seo-description: Atributo de configuração para o visualizador do Video360.
seo-title: SocialShare.bear
solution: Experience Manager
title: SocialShare.bear
topic: Dynamic media
uuid: 43217e2e-71c5-4c58-94e0-c6ed38e25a5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SocialShare.bear{#socialshare-bearing}

Atributo de configuração para o visualizador do Video360.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> para cima|para baixo|para a esquerda|para a direita|vertical|lateral em forma de encaixe</span> </p> </td> 
   <td colname="col2"> <p> Especifica a direção da animação do slide para o container de botões. </p> <p> Quando definido para <span class="codeph"> cima</span>, <span class="codeph"> baixo</span>, <span class="codeph"> esquerda</span>ou <span class="codeph"> direita</span>, o painel é lançado em uma direção especificada, sem uma verificação adicional de limites, o que pode resultar no recorte do painel por um container externo. </p> <p>Quando definido para <span class="codeph"> ajuste vertical</span>, o componente primeiro alterna a posição do painel base para a parte inferior do SocialShare e tenta implantar o painel na parte inferior, direita ou esquerda desse local base. A cada tentativa, o componente verifica se o painel está cortado por um container externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para a parte superior e repetir as tentativas de roll-out na direção superior, direita e esquerda. </p> <p>Quando definido para <span class="codeph"> lateral</span>, o componente usa uma lógica semelhante. No entanto, ele desloca a base para a direita primeiro, tentando as direções de implantação direita, para baixo e para cima, e então desloca a base para a esquerda, tentando as direções de implantação esquerda, para baixo e para cima. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Example {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```

