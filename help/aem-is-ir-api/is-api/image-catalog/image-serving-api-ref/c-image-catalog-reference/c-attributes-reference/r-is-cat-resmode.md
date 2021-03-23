---
description: Modo de reamostragem padrão. Especifica a reamostragem e os atributos de interpolação padrão a serem usados para dimensionar dados de imagem.
seo-description: Modo de reamostragem padrão. Especifica a reamostragem e os atributos de interpolação padrão a serem usados para dimensionar dados de imagem.
seo-title: ResMode
solution: Experience Manager
title: ResMode
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# ResMode{#resmode}

Modo de reamostragem padrão. Especifica a reamostragem e os atributos de interpolação padrão a serem usados para dimensionar dados de imagem.

Usado quando `resMode=` não é especificado em uma solicitação.

## Propriedades {#section-493f900be522486f97710cebdc4460c2}

Enum. Defina como 2 para `bilin`, 3 para `bicub` ou 4 para `sharp2` modo de interpolação (consulte ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` para obter detalhes). `sharp` (1) está sendo substituído. Use `sharp2` (4) em vez de melhores resultados.

## Padrão {#section-35f980e745fc4d79a2621e8abacc724d}

Herdado de `default::ResMode` se não estiver definido ou se estiver vazio.

## Consulte também {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
