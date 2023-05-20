---
description: TTL de cache do cliente para respostas que não são de imagem. Fornece o intervalo de expiração para determinadas respostas que não sejam de imagem.
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# NonImgExpiration{#nonimgexpiration}

TTL de cache do cliente para respostas que não são de imagem. Fornece o intervalo de expiração para determinadas respostas que não sejam de imagem.

Fornece o intervalo de expiração para determinadas respostas que não são de imagens, incluindo aquelas enviadas em resposta aos seguintes comandos:

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Propriedades {#section-d37e3113f4b1468b86b5a14e80d94c83}

Número real, 0 ou maior. Número de horas até a expiração desde que os dados de resposta foram gerados. Defina como 0 para sempre expirar a imagem de resposta imediatamente, o que desativa efetivamente o cache do cliente para respostas de imagem padrão. Defina como -1 para marcar como *nunca expira*.

## Padrão {#section-96981360c0234b7f824d2ff7c25a7954}

Herdado de `default::NonImgExpiration` se não estiver definido ou se estiver vazio.

TTL (Time-To-Live) é a duração antes do cache expirar. O TTL padrão é de 6 minutos.

## Consulte também {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catálogo::Expiração](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
