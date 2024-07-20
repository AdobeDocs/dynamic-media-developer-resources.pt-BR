---
title: SocialShare.bearing
description: Atributo de configuração para o Visualizador de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 391efc4e-23f6-4159-8b03-ad1c9a887ec3
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# SocialShare.bearing{#socialshare-bearing}

Atributo de configuração para o Visualizador de vídeo.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> para cima|para baixo|esquerda|direita|ajuste vertical|ajuste lateral</span> </p> </td> 
   <td colname="col2"> <p> Especifica a direção da animação do slide para o contêiner de botões. </p> <p> Quando definido como <span class="codeph"> up</span>, <span class="codeph"> down</span>, <span class="codeph"> left</span> ou <span class="codeph"> right</span>, o painel é implantado em uma direção especificada sem uma verificação de limites extras, o que pode resultar no recorte do painel por um contêiner externo. </p> <p>Quando definido como <span class="codeph"> fit-vertical</span>, o componente primeiro desloca a posição do painel base para a parte inferior do SocialShare e tenta implantar o painel a partir da parte inferior, direita ou esquerda desse local base. A cada tentativa, o componente verifica se o painel está recortado por um contêiner externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para o topo e repetir as tentativas de implantação no canto superior, direito e esquerdo. </p> <p>Quando definido como <span class="codeph"> fit-lateral</span>, o componente usa uma lógica semelhante. No entanto, ele desloca a base para a direita primeiro, tentando as direções de implantação para a direita, para baixo e para cima e, em seguida, desloca a base para a esquerda, tentando as direções de implantação para a esquerda, para baixo e para cima. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propriedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Padrão {#section-d016470e92a74f98a18c4ab3489410a5}

`fit-vertical`

## Exemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
bearing=left
```
