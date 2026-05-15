---
title: PolíticaDeValidaçãoDeCache
description: Política de validação de cache do servidor. Especifica quando as entradas de cache do servidor são validadas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d54a8ab9-d6b3-4eae-95c6-c4ab6f00ebde
TQID: 'https://experienceleague.adobe.com/s7dYUadAD1i1ROqCafEZOa5Tztl3ss2HAXnEsPiRGr8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 0%

---

# PolíticaDeValidaçãoDeCache{#cachevalidationpolicy}

Política de validação de cache do servidor. Especifica quando as entradas de cache do servidor são validadas.

Com a validação baseada em expiração, as imagens de origem são periodicamente verificadas se foram alteradas. Com a validação baseada em catálogo, as imagens de origem são verificadas somente após a alteração do valor `catalog::TimeStamp`.

A validação baseada em catálogo é recomendada quando catálogos de imagem são usados. A validação baseada em expiração deve ser usada quando as imagens são referenciadas diretamente, sem o uso de um catálogo de imagens.

## Propriedades {#section-650cbddd81a24c3b8b70479248a45dc9}

Enum. 0 para selecionar validação baseada em expiração, 1 para selecionar validação de cache baseada em catálogo.

## Padrão {#section-0ce22732e0e9431d8a05d8b9158c0b5a}

Herdado de `default::CacheValidationPolicy` se não estiver definido ou se estiver vazio.

## Consulte também {#section-a0c922fa519641f2bce05e75e4eb51d0}

[catálogo::Carimbo de data/hora](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-timestamp-svg.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
