---
description: Imagem de resposta padrão. Especifica a entrada de imagem ou catálogo a ser usada caso um arquivo de imagem não seja encontrado e defaultImage= não seja especificado na solicitação.
solution: Experience Manager
title: ImagemPadrão
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2044b447-0ee1-4964-b751-8637c5e115d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# ImagemPadrão{#defaultimage}

Imagem de resposta padrão. Especifica a entrada de imagem ou catálogo a ser usada caso um arquivo de imagem não seja encontrado e defaultImage= não seja especificado na solicitação.

Pode ser uma entrada de catálogo (incluindo um modelo) ou um caminho de arquivo de imagem relativo (a `attribute::RootPath`) ou absoluto. Útil para substituir imagens ausentes por imagens padrão.

## Propriedades {#section-b6d8193827c34e5f948792aba8b8daaf}

String de texto. Se especificado, deve ser um valor `catalog::Id` válido neste catálogo de imagens ou um caminho relativo (para `attribute::RootPath`) ou absoluto para um arquivo de imagem acessível pelo Servidor de Imagens.

## Restrições {#section-5d8ea872f0b0415fbd3a83410bbcf512}

As fontes de imagem estrangeiras não são cobertas pelo mecanismo de imagem padrão; um erro é retornado se uma fonte de imagem estrangeira não for válida.

## Padrão {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

Herdado de `default::DefaultImage` se não estiver definido. Se definido, mas vazio, o comportamento de imagem padrão é desabilitado, mesmo se `default::DefaultImage` for definido.

## Consulte também {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782), [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
