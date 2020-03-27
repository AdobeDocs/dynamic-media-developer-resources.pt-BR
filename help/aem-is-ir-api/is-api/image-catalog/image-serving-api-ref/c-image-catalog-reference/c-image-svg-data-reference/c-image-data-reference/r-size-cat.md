---
description: Tamanho da imagem. Tamanho em pixels da imagem de resolução completa referenciada pelo Caminho do catálogo.
seo-description: Tamanho da imagem. Tamanho em pixels da imagem de resolução completa referenciada pelo Caminho do catálogo.
seo-title: Tamanho
solution: Experience Manager
title: Tamanho
topic: Scene7 Image Serving - Image Rendering API
uuid: 6fe2aeb6-0dd7-4631-955f-ad74d11b613d
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# Tamanho{#size}

Tamanho da imagem. Tamanho de pixel da imagem de resolução completa referenciada pelo catálogo::Path.

Se esse valor for fornecido, o Serviço de imagem o usará para evitar a necessidade de abrir a imagem para obter o tamanho real da imagem.

>[!NOTE]
>
>Se `catalog::Size`for fornecido e não for o mesmo que o tamanho real da imagem de resolução completa, pode resultar um comportamento indefinido.

## Propriedades {#section-5c914ec8b1444a8e99d811b647cd42a3}

Dois números inteiros, cada um maior que 0, separados por uma vírgula. Opcional.

## Padrão {#section-257c6d47cf314ef0b3c3c32b18f0f0f1}

Se o campo não estiver presente ou se o campo estiver vazio, o tamanho real da imagem será usado.

## Consulte também {#section-e63797357d5a4119a10db1e6e088f6e9}

[catálogo::Caminho](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md#reference-306afcaff172440ca81b85da8d78213c) , [res=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md)
