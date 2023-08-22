---
title: xmpEmbed
description: Incorporar metadados de XMP. Especifica se os metadados de XMP devem ser incluídos na imagem de resposta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# xmpEmbed{#xmpembed}

Incorporar metadados de XMP. Especifica se os metadados de XMP devem ser incluídos na imagem de resposta.

`xmpEmbed=0|1`

>[!NOTE]
>
>Os dados do XMP são passados da imagem de origem para a imagem de resposta sem modificação. Isso pode resultar na incorporação de dados incorretos na imagem de resposta.

## Propriedades {#section-27024c4272f44d9a8c264a0629193af2}

Solicitar atributo. Ignorado se a imagem de origem não contiver dados de XMP. Somente dados de XMP da imagem de origem de `layer=0` são processados. Dados de XMP de outras imagens de camada são ignorados.

Ignorado se o formato de imagem de saída não suportar a incorporação do XMP. Consulte a descrição de `fmt=` para obter uma lista de formatos de imagem de saída que oferecem suporte à incorporação do XMP.

## Padrão {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, para nenhuma incorporação de caminhos em imagens de saída.

## Consulte também {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
