---
description: Âncora de imagem. Especifica o ponto de ancoragem (ponto de acesso) de uma textura repetível, borda de parede ou imagem de decalque.
solution: Experience Manager
title: Âncora
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1336330e-86e5-418d-bea3-0c09368e3528
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Âncora{#anchor}

Âncora de imagem. Especifica o ponto de ancoragem (ponto de acesso) de uma textura repetível, borda de parede ou imagem de decalque.

Uma textura repetível é aplicada a um objeto de vinheta para que o ponto de ancoragem da textura esteja localizado no ponto de origem da textura do objeto. Uma imagem de decalque é aplicada a um objeto de vinheta para que o ponto de ancoragem do decalque esteja localizado no ponto de origem do decalque do objeto. Para bordas de parede, somente o valor x é usado; o valor y é ignorado.

## Propriedades {#section-bc4bc8b897c64535b88681e57d72942f}

Dois números inteiros, separados por vírgula. Deslocamento de pixel em relação ao canto superior esquerdo da imagem. Ignorado se `catalog::Alignment=3` e por materiais de gabinete e cores sólidas.

## Padrão {#section-b7ccc419a356415294706cd295ae96c9}

Se o campo estiver vazio ou ausente, o canto superior esquerdo (0,0) da imagem para materiais de textura repetíveis é usado, ou o centro da imagem no caso de materiais de decalque.

## Consulte também {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catálogo::Alinhamento](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [âncora=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
