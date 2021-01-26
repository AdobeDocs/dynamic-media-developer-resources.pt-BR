---
description: Âncora de imagem. Especifica o ponto de ancoragem (ponto de acesso) de uma textura repetível, borda de parede ou imagem de decal.
seo-description: Âncora de imagem. Especifica o ponto de ancoragem (ponto de acesso) de uma textura repetível, borda de parede ou imagem de decal.
seo-title: Âncora
solution: Experience Manager
title: Âncora
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0b1a0fea-b299-44dc-b9fd-5916130b2ef3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# Âncora{#anchor}

Âncora de imagem. Especifica o ponto de ancoragem (ponto de acesso) de uma textura repetível, borda de parede ou imagem de decal.

Uma textura repetível é aplicada a um objeto de vinheta para que o ponto de ancoragem da textura fique localizado no ponto de origem da textura do objeto. Uma imagem decal é aplicada a um objeto de vinheta para que o ponto de ancoragem decal esteja localizado no ponto de origem decal do objeto. Para as fronteiras de parede, apenas é utilizado o valor x; o valor y é ignorado.

## Propriedades {#section-bc4bc8b897c64535b88681e57d72942f}

Dois números inteiros, separados por vírgula. Deslocamento de pixel em relação à parte superior esquerda da imagem. Ignorado se `catalog::Alignment=3` e por cor sólida e materiais de gabinete.

## Padrão {#section-b7ccc419a356415294706cd295ae96c9}

Se o campo estiver vazio ou não estiver presente, o canto superior esquerdo (0,0) da imagem para materiais de textura repetíveis será usado ou o centro da imagem no caso de materiais de decalque.

## Consulte também {#section-3fb2ce2f6b7240a4b6f4858022a0a01d}

[catálogo::Alinhamento](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [âncora=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
