---
description: Tempo de funcionamento padrão do cache do cliente. Fornece um intervalo de expiração padrão caso um registro de catálogo específico não contenha um valor válido de Expiração do catálogo.
seo-description: Tempo de funcionamento padrão do cache do cliente. Fornece um intervalo de expiração padrão caso um registro de catálogo específico não contenha um valor válido de Expiração do catálogo.
seo-title: Expiração
solution: Experience Manager
title: Expiração
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 26b2abee-8bd1-4011-90ff-f5143826ac0d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# Expiração{#expiration}

Tempo de funcionamento padrão do cache do cliente. Fornece um intervalo de expiração padrão no caso de um registro de catálogo específico não conter um valor de catálogo válido::Expiration.

## Propriedades {#section-063be3b2f13a48a3a5ab8080718e9812}

Número real, 0 ou maior. Número de horas até a expiração desde que os dados de resposta foram gerados. Defina como 0 para sempre expirar a imagem de resposta imediatamente, o que efetivamente desativa o cache do cliente. Defina como -1 para marcar como `never expire`.

## Padrão {#section-f55308b195c04083996f6717c8537634}

Herdado de `default::Expiration` se não estiver definido ou se estiver vazio.

TTL (Time-To-Live) é a duração antes da expiração do cache. O TTL padrão é de 10 horas.

## Consulte também {#section-b2411d99ddb14115ad475d506efd8967}

[catálogo::Expiração](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [atributo::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [atributo::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
