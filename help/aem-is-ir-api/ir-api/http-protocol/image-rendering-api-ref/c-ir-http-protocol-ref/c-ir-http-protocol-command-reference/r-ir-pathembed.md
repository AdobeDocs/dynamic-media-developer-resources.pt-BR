---
description: Incorporar dados de caminhos. Especifica se os caminhos do Photoshop incorporados na vinheta devem ser incluídos na imagem de resposta.
seo-description: Incorporar dados de caminhos. Especifica se os caminhos do Photoshop incorporados na vinheta devem ser incluídos na imagem de resposta.
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
uuid: d40ea1b5-f2d3-4f81-b96f-abb4eb7eb2b3
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---


# pathEmbed{#pathembed}

Incorporar dados de caminhos. Especifica se os caminhos do Photoshop incorporados na vinheta devem ser incluídos na imagem de resposta.

`pathEmbed=0|1`

## Propriedades {#section-be50b6d1ebd14a9c93f80ac338b44bfc}

Atributo da solicitação. Ignorado se a vinheta não contiver dados de caminhos. Os dados dos caminhos são dimensionados para `wid=` e/ou `hei=` se necessário.

Ignorado se o formato de imagem de saída não oferecer suporte para incorporação de caminho. Consulte a descrição de `fmt=` para obter uma lista de formatos de imagem de saída que oferecem suporte para incorporação de caminho.

## Padrão {#section-3be88ed9053b48919ff33af9418078cc}

`pathEmbed=0`, para não incorporar caminhos em imagens de saída.

## Consulte também {#section-4e6151658c384b6f9d0446f55dde7b7f}

[fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
