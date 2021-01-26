---
description: Incorporar dados de caminhos. Especifica se os caminhos Photoshop incorporados na vinheta devem ser incluídos na imagem de resposta.
seo-description: Incorporar dados de caminhos. Especifica se os caminhos Photoshop incorporados na vinheta devem ser incluídos na imagem de resposta.
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d40ea1b5-f2d3-4f81-b96f-abb4eb7eb2b3
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---


# pathEmbed{#pathembed}

Incorporar dados de caminhos. Especifica se os caminhos Photoshop incorporados na vinheta devem ser incluídos na imagem de resposta.

`pathEmbed=0|1`

## Propriedades {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Atributo de solicitação. Ignorado se a vinheta não contém dados de caminhos. Os dados de caminhos são dimensionados para `wid=` e/ou `hei=`, se necessário.

Ignorado se o formato de imagem de saída não oferecer suporte para incorporação de caminho. Consulte a descrição de `fmt=` para obter uma lista de formatos de imagem de saída compatíveis com a incorporação de caminhos.

## Padrão {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, para não incorporar caminhos em imagens de saída.

## Consulte também {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
