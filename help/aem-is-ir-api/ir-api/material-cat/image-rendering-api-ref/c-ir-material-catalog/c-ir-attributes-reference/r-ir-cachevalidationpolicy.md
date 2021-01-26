---
description: Política de validação do cache do servidor. Especifica quando as entradas de cache do lado do servidor são validadas.
seo-description: Política de validação do cache do servidor. Especifica quando as entradas de cache do lado do servidor são validadas.
seo-title: CacheValidationPolicy
solution: Experience Manager
title: CacheValidationPolicy
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 299dd5fe-9a0c-43df-a4c8-6b9e9c24003b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# CacheValidationPolicy{#cachevalidationpolicy}

Política de validação do cache do servidor. Especifica quando as entradas de cache do lado do servidor são validadas.

Com a validação baseada em expiração, os materiais de origem e as vinhetas são periodicamente verificados para ver se foram alterados. Com a validação baseada em catálogo, as imagens de origem são verificadas somente depois que o valor `catalog::TimeStamp` é alterado.

A validação baseada em catálogo é recomendada quando os catálogos de material e de vinheta são usados. A validação baseada em expiração deve ser usada quando as vinhetas são referenciadas em solicitações de Renderização de imagem diretamente pelo caminho.

## Propriedades {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 para selecionar a validação baseada em expiração. 1 para selecionar a validação de cache baseada em catálogo.

## Padrão {#section-e09f3af8b6b3497d963199988dc5345d}

Herdado de `default::CacheValidationPolicy` se não estiver definido ou se estiver vazio.

## Consulte também {#section-b374e4d908e24af8995b2b376ca1be8b}

[catálogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
