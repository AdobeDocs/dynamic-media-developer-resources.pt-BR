---
description: Modo de reamostragem padrão. Especifica a reamostragem e os atributos de interpolação padrão a serem usados para dimensionar dados de imagem.
seo-description: Modo de reamostragem padrão. Especifica a reamostragem e os atributos de interpolação padrão a serem usados para dimensionar dados de imagem.
seo-title: ResMode
solution: Experience Manager
title: ResMode
topic: Scene7 Image Serving - Image Rendering API
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ResMode{#resmode}

Modo de reamostragem padrão. Especifica a reamostragem e os atributos de interpolação padrão a serem usados para dimensionar dados de imagem.

Usado quando não `resMode=` é especificado em uma solicitação.

## Propriedades {#section-493f900be522486f97710cebdc4460c2}

Enum. Defina para 2 para `bilin`, 3 para `bicub`ou 4 para o modo de `sharp2` interpolação (consulte ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` para obter detalhes). `sharp` (1) está sendo substituído. Use `sharp2` (4) como alternativa para obter melhores resultados.

## Padrão {#section-35f980e745fc4d79a2621e8abacc724d}

Herdado de `default::ResMode` se não estiver definido ou se estiver vazio.

## Consulte também {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
