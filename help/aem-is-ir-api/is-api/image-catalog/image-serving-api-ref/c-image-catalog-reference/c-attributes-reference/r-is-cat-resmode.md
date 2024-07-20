---
title: ResMode
description: Modo de reamostragem padrão. Especifica os atributos padrão de reamostragem e interpolação a serem usados para dimensionar dados de imagem.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# ResMode{#resmode}

Modo de reamostragem padrão. Especifica os atributos padrão de reamostragem e interpolação a serem usados para dimensionar dados de imagem.

Usado quando `resMode=` não é especificado em uma solicitação.

## Propriedades {#section-493f900be522486f97710cebdc4460c2}

Enum. Defina como 2 para `bilin`, 3 para `bicub` ou 4 para o modo de interpolação `sharp2` (consulte [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) para obter detalhes). `sharp` (1) está sendo descontinuado. Em vez disso, use `sharp2` (4) para obter melhores resultados.

## Padrão {#section-35f980e745fc4d79a2621e8abacc724d}

Herdado de `default::ResMode` se não estiver definido ou se estiver vazio.

## Consulte também {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
