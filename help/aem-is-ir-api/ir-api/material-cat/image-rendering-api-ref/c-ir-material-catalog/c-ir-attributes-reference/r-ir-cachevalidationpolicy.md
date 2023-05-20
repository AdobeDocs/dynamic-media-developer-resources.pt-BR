---
title: PolíticaDeValidaçãoDeCache
description: Política de validação de cache do servidor. Especifica quando as entradas de cache do servidor são validadas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e52577ba-d085-41f5-ad15-48e5a319e344
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# PolíticaDeValidaçãoDeCache{#cachevalidationpolicy}

Política de validação de cache do servidor. Especifica quando as entradas de cache do servidor são validadas.

Com a validação baseada em expiração, os materiais de origem e as vinhetas são verificados periodicamente para ver se foram alterados. Com a validação baseada em catálogo, as imagens de origem são verificadas somente após a `catalog::TimeStamp` valor alterado.

A validação baseada em catálogo é recomendada quando são usados catálogos de material e vinheta. A validação baseada em expiração deve ser usada quando as vinhetas são referenciadas nas solicitações de Renderização de imagem diretamente pelo caminho.

## Propriedades {#section-46e13cb341eb442c86e0d8292de23ea0}

Enum. 0 para selecionar a validação baseada em expiração. 1 para selecionar a validação do cache com base em catálogo.

## Padrão {#section-e09f3af8b6b3497d963199988dc5345d}

Herdado de `default::CacheValidationPolicy` se não estiver definido ou se estiver vazio.

## Consulte também {#section-b374e4d908e24af8995b2b376ca1be8b}

[catálogo::Carimbo de data/hora](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319)
