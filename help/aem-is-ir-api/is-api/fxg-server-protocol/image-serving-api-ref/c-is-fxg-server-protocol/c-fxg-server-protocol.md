---
title: Protocolo de servidor FXG
description: Para manipular um gráfico, é possível usar pontos de referência semelhantes a pontos de bússola.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 0%

---

# Protocolo de servidor FXG{#fxg-server-protocol}

Para manipular um gráfico, é possível usar pontos de referência semelhantes a pontos de bússola.

Usando pontos de referência, você pode girar, dimensionar ou redimensionar um gráfico em relação a um ponto de referência específico. Os pontos de referência `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south`, e `southeast`. Por exemplo, usando o ponto de referência central, é possível girar um gráfico 45° em seu centro. A imagem a seguir mostra onde estão localizados os pontos de referência, um gráfico, o gráfico rotacionado 20° a partir de seu `northWest` ponto de referência, e o gráfico girou 20° em relação ao seu `east` referência.

![Imagem de pontos de referência](assets/wp_ref_points.png)

* A. Localizações dos pontos de referência
* B. Um gráfico
* C. O gráfico girou 20° em relação ao seu `northWest` ponto de referência
* D. O gráfico girou 20° em relação ao seu `east` ponto de referência

A sintaxe é:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

O valor padrão é none. A variável `inherit` o valor passa o `s7:referencePoint` desde que não seja `none`, da parte superior da página ou nível de grupo para todos os filhos. A variável `none` Configurar significa que não há ponto de referência para o objeto e o sistema de coordenadas FXG é usado.

>[!NOTE]
>
>Para usar um ponto de referência e não ter nenhum deslocamento no objeto após sua manipulação, atualize os valores x e y do objeto após manipulá-lo.

Quando um valor de `s7:referencePoint` for usada com grupos (ou caminhos, elementos de linha ou qualquer elemento que não tenha definições explícitas de largura e altura), o valor se aplicará à caixa delimitadora cumulativa do grupo. Por exemplo, o ponto superior esquerdo da caixa delimitadora de todos os objetos no grupo serve como `northWest` ponto de referência para o grupo; o ponto inferior direito serve de `southEast` referência.
