---
title: SocialShare.bearing
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# SocialShare.bearing{#socialshare-bearing}

Atributo de configuração para o Visualizador de vídeo interativo.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> para cima|para baixo|esquerda|direita|ajuste vertical|ajuste lateral</span> </p> </td> 
   <td colname="col2"> <p> Especifica a direção da animação do slide para o contêiner de botões. Quando definido como <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> ou <span class="codeph"> right</span>, o painel é implantado na direção especificada sem nenhuma verificação de limites adicionais, o que pode resultar no recorte do painel por um contêiner externo. </p> <p>Quando definido como <span class="codeph"> fit-vertical</span>, o componente primeiro desloca a posição do painel base para a parte inferior do SocialShare. Em seguida, ele tenta implantar o painel em uma das seguintes direções a partir desse local base: inferior, direita, esquerda. A cada tentativa, o componente verifica se o painel é recortado por um contêiner externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para o topo e repetirá as tentativas de implantação de cima, direita e esquerda. </p> <p>Quando definido como <span class="codeph"> fit-lateral</span>, o componente usa uma lógica semelhante, mas altera a base para a direita primeiro, tentando as direções de implantação para a direita, para baixo e para cima. Em seguida, desloca a base para a esquerda, tentando as direções de implantação para a esquerda, para baixo e para cima. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Padrão {#section-71fb773f814649b2885aefee68073641}

`fit-vertical`

## Exemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
bearing=left
```
