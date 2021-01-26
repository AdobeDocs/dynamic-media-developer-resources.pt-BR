---
description: Incorporar metadados XMP. Especifica se os metadados XMP devem ser incluídos na imagem de resposta.
seo-description: Incorporar metadados XMP. Especifica se os metadados XMP devem ser incluídos na imagem de resposta.
seo-title: xmpEmbed
solution: Experience Manager
title: xmpEmbed
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c0dfd0e5-16d1-4a6e-957a-ecc276b9361a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---


# xmpEmbed{#xmpembed}

Incorporar metadados XMP. Especifica se os metadados XMP devem ser incluídos na imagem de resposta.

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP dados são passados da imagem de origem para a imagem de resposta sem modificação. Isso pode resultar na incorporação de dados incorretos na imagem de resposta.

## Propriedades {#section-27024c4272f44d9a8c264a0629193af2}

Atributo de solicitação. Ignorado se a imagem de origem não contiver dados XMP. Somente dados XMP da imagem de origem de `layer=0` são processados. XMP dados de outras imagens de camada são ignorados.

Ignorado se o formato de imagem de saída não suportar XMP incorporação. Consulte a descrição de `fmt=` para obter uma lista de formatos de imagem de saída compatíveis com a incorporação XMP.

## Padrão {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, para não incorporar caminhos em imagens de saída.

## Consulte também {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
