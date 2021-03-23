---
description: Atributo de configuração para o visualizador do Video360.
seo-description: Atributo de configuração para o visualizador do Video360.
seo-title: SocialShare.bearing
solution: Experience Manager
title: SocialShare.bearing
uuid: 43217e2e-71c5-4c58-94e0-c6ed38e25a5b
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeo 360 VR
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---


# SocialShare.bearing{#socialshare-bearing}

Atributo de configuração para o visualizador do Video360.

`[SocialShare.|<containerId>_socialShare.]bearing=up|down|left|right|fit-vertical|fit-lateral`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> para cima|para baixo|para a esquerda|para a direita|para-vertical|para-caber-lateral</span> </p> </td> 
   <td colname="col2"> <p> Especifica a direção da animação de slides para o contêiner de botões. </p> <p> Quando definido para <span class="codeph"> para cima</span>, <span class="codeph"> para baixo</span>, <span class="codeph"> para a esquerda</span> ou <span class="codeph"> para a direita</span>, o painel é implantado em uma direção especificada sem uma verificação de limites adicional, o que pode resultar em recorte de painel por um contêiner externo. </p> <p>Quando definido como <span class="codeph"> fit-vertical</span>, o componente primeiro alterna a posição do painel base para a parte inferior do SocialShare e tenta implantar o painel da parte inferior, direita ou esquerda desse local base. A cada tentativa, o componente verifica se o painel está cortado por um contêiner externo. Se todas as tentativas falharem, o componente tentará deslocar a posição do painel base para a parte superior e repetir as tentativas de implantação na direção superior, direita e esquerda. </p> <p>Quando definido como <span class="codeph"> fit-lateral</span>, o componente usa uma lógica semelhante. No entanto, ele desloca a base para a direita primeiro, tentando para a direita, para baixo e para cima em direções de implementação, e então alterna a base para a esquerda, tentando para a esquerda, para baixo e para cima em direções de implementação. </p> </td> 
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

