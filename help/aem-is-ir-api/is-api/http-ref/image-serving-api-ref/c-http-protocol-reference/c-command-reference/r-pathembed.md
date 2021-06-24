---
description: Incorporar dados de caminhos. Especifica se os caminhos Photoshop da camada 0 da imagem de origem devem ser incluídos na imagem de resposta.
solution: Experience Manager
title: pathEmbed
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: a3b305eb-0313-4c58-bd47-4f87e09d0e0b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# pathEmbed{#pathembed}

Incorporar dados de caminhos. Especifica se os caminhos Photoshop da camada 0 da imagem de origem devem ser incluídos na imagem de resposta.

`pathEmbed=0|1`

## Propriedades {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Atributo da solicitação. Ignorado se a imagem de origem não contiver dados de caminhos. Os dados de caminhos são dimensionados e girados como os dados da imagem. Somente caminhos da imagem de origem de `layer=0` são processados; caminhos de outras imagens de camada são ignorados.

Ignorado se o formato de imagem de saída não oferecer suporte para incorporação de caminho. Consulte a descrição de `fmt=` para obter uma lista de formatos de imagem de saída que oferecem suporte para incorporação de caminho.

## Restrições {#section-697cddb79a1542bc8457d2f4f59eec69}

Caminhos Photoshop abertos (caminhos que não formam loops fechados) não são suportados para incorporação na imagem de resposta no momento.

## Padrão {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, para não incorporar caminhos em imagens de saída.

## Consulte também {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
