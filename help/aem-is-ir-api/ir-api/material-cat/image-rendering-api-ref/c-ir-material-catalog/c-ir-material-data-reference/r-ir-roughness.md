---
description: Rugosidade da superfície. Especifica a luminosidade relativa da superfície do material. Usado em conjunto com o Tipo de catálogo e o Brilho de catálogo para controlar efeitos de renderização de reflexão 3D.
solution: Experience Manager
title: Rugosidade
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 61d956ec-62dd-4879-877e-2ac422396e2e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# Rugosidade{#roughness}

Rugosidade da superfície. Especifica a luminosidade relativa da superfície do material. Usado em conjunto com catalog::Type e catalog::Gloss para controlar efeitos de renderização de reflexão 3D.

## Propriedades {#section-70c3f2394fd8477ca83a369448907971}

Número inteiro. Valor percentual no intervalo de 0 a 100. Opcional para todos os materiais. Usado apenas para vinhetas com vários mapas de reflexão ou vinhetas com recurso de reflexão 3D. Deixe vazio ou defina -1 se não for conhecido ou não for necessário.

## Padrão {#section-c6d5c0613a8745ddbd9f43c8c90b1580}

-1; um padrão de servidor é usado.

## Consulte também {#section-d08b59eb76824226b89c6fdf86bb5ce5}

[áspero=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180) , [catálogo::Brilho](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb), [catálogo::Tipo](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
