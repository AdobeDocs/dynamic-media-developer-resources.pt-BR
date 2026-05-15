---
title: SocialShare.Bearing
description: Atributo de configuração para o Visualizador de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 391efc4e-23f6-4159-8b03-ad1c9a887ec3
TQID: 'https://experienceleague.adobe.com/YhNrijfrkxHpLzZFMRr2AdjFARJ8E5xSaTfhANHbXGo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 185
ht-degree: 0%

---

# SocialShare.Bearing{#socialshare-bearing}

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
