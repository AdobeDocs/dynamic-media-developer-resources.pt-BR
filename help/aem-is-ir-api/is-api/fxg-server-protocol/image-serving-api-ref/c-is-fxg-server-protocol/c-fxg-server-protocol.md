---
description: Para manipular um gráfico, você pode usar pontos de referência semelhantes a pontos de bússola.
seo-description: Para manipular um gráfico, você pode usar pontos de referência semelhantes a pontos de bússola.
seo-title: Protocolo do servidor FXG
solution: Experience Manager
title: Protocolo do servidor FXG
uuid: 5cb123ca-2274-4ddb-8fa1-ab22a19172f6
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---


# Protocolo do servidor FXG{#fxg-server-protocol}

Para manipular um gráfico, você pode usar pontos de referência semelhantes a pontos de bússola.

Usando pontos de referência, você pode girar, dimensionar ou redimensionar um gráfico em relação a um ponto de referência específico. Os pontos de referência são `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` e `southeast`. Por exemplo, usando o ponto de referência central, é possível girar um gráfico em 45 graus no centro. Esta ilustração mostra onde estão os pontos de referência, um gráfico, o gráfico girado 20 graus a partir do seu ponto de referência `northWest` e o gráfico girado 20 graus a partir do seu ponto de referência `east`.

![](assets/wp_ref_points.png)

* A. Locais dos pontos de referência
* B. Gráfico A
* C. O gráfico rotacionou 20 graus a partir do seu ponto de referência `northWest`
* D. O gráfico rotacionou 20 graus a partir do seu ponto de referência `east`

A sintaxe é:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

O valor padrão é nenhum. O valor `inherit` passa o valor `s7:referencePoint`, desde que não seja `none`, da parte superior da página ou do nível do grupo para todos os filhos. A configuração `none` significa que não há um ponto de referência para o objeto e o sistema de coordenadas FXG é usado.

>[!NOTE]
>
>Para usar um ponto de referência e não ter nenhum deslocamento no objeto após ele ser manipulado, atualize os valores x e y do objeto depois de manipulá-lo.

Quando um valor de `s7:referencePoint` é usado com grupos (ou caminhos, elementos de linha ou qualquer elemento que não tenha definições explícitas de largura e altura), o valor se aplica à caixa delimitadora cumulativa do grupo. Por exemplo, o ponto superior esquerdo da caixa delimitadora de todos os objetos do grupo serve como o ponto de referência `northWest` para o grupo; o ponto inferior direito serve como o ponto de referência `southEast`.

