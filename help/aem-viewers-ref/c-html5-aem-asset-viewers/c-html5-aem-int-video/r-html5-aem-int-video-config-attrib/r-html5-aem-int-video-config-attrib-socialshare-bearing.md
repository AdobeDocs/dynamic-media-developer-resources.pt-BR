---
description: Atributo de configuração para o Visualizador de vídeo interativo.
solution: Experience Manager
title: SocialShare.bearing
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interativos
role: Developer,Business Practitioner
exl-id: f34d6954-01c5-49e0-94d4-fd577c57956e
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# SocialShare.bearing{#socialshare-bearing}

Atributo de configuração para o Visualizador de vídeo interativo.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> para cima|para baixo|para a esquerda|para a direita|para-vertical|para-caber-lateral</span> </p> </td> 
   <td colname="col2"> <p> Especifica a direção da animação de slide para o contêiner de botões. Quando definido para <span class="codeph"> para cima</span>, <span class="codeph"> para baixo</span>, <span class="codeph"> para a esquerda</span> ou <span class="codeph"> para a direita</span>, o painel é implantado na direção especificada sem qualquer verificação de limites adicional, o que pode resultar no recorte do painel por um contêiner externo. </p> <p>Quando definido como <span class="codeph"> fit-vertical</span>, o componente primeiro alterna a posição do painel base para a parte inferior do SocialShare e tenta implantar o painel em uma das seguintes direções a partir de um local base como esse: de baixo, à direita, à esquerda. A cada tentativa, o componente verifica se o painel está cortado por um contêiner externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para o topo e repetirá as tentativas de implantação de uma direção superior, direita e esquerda. </p> <p>Quando definido como <span class="codeph"> fit-lateral</span>, o componente usa uma lógica semelhante, mas alterna a base para a direita primeiro, tentando as direções de distribuição para a direita, para baixo e para cima. Em seguida, ele muda a base para a esquerda, tentando a esquerda, para baixo e para cima em direções de implantação. </p> </td> 
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
