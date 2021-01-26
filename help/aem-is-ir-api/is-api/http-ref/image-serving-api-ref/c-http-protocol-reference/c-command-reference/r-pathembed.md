---
description: Incorporar dados de caminhos. Especifica se os caminhos do Photoshop do arquivo de imagem de origem da camada 0 devem ser incluídos na imagem de resposta.
seo-description: Incorporar dados de caminhos. Especifica se os caminhos do Photoshop do arquivo de imagem de origem da camada 0 devem ser incluídos na imagem de resposta.
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 93e63c7c-c091-4bb1-baff-45706fd611ea
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# pathEmbed{#pathembed}

Incorporar dados de caminhos. Especifica se os caminhos do Photoshop do arquivo de imagem de origem da camada 0 devem ser incluídos na imagem de resposta.

`pathEmbed=0|1`

## Propriedades {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Atributo de solicitação. Ignorado se a imagem de origem não contiver dados de caminhos. Os dados de caminhos são dimensionados e girados como os dados da imagem. Somente caminhos da imagem de origem de `layer=0` são processados; caminhos de outras imagens de camada são ignorados.

Ignorado se o formato de imagem de saída não oferecer suporte para incorporação de caminho. Consulte a descrição de `fmt=` para obter uma lista de formatos de imagem de saída compatíveis com a incorporação de caminhos.

## Restrições {#section-697cddb79a1542bc8457d2f4f59eec69}

Caminhos abertos do Photoshop (caminhos que não formam loops fechados) não são suportados para incorporação na imagem de resposta no momento.

## Padrão {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, para não incorporar caminhos em imagens de saída.

## Consulte também {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
