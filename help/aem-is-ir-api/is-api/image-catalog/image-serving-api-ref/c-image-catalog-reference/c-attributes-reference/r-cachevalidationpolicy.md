---
title: CacheValidationPolicy
description: Política de validação do cache do servidor. Especifica quando as entradas de cache do lado do servidor são validadas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# CacheValidationPolicy{#cachevalidationpolicy}

Política de validação do cache do servidor. Especifica quando as entradas de cache do lado do servidor são validadas.

Com a validação baseada em expiração, as imagens de origem são verificadas periodicamente se foram alteradas. Com validação baseada em catálogo, as imagens de origem são marcadas somente após a variável `catalog::TimeStamp` valor alterado.

A validação baseada em catálogo é recomendada quando os catálogos de imagem são usados. A validação baseada em expiração deve ser usada quando as imagens são referenciadas diretamente, sem o uso de um catálogo de imagens.

## Propriedades {#section-650cbddd81a24c3b8b70479248a45dc9}

Enum. 0 para selecionar a validação baseada em expiração, 1 para selecionar a validação de cache baseada em catálogo.

## Padrão {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Herdado de `default::CacheValidationPolicy` se não estiver definido ou se estiver vazio.

## Consulte também {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catálogo::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
