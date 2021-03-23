---
description: TTL do cache do cliente para respostas que não sejam de imagem. Fornece o intervalo de expiração para determinadas respostas que não são de imagem.
seo-description: TTL do cache do cliente para respostas que não sejam de imagem. Fornece o intervalo de expiração para determinadas respostas que não são de imagem.
seo-title: NonImgExpiration
solution: Experience Manager
title: NonImgExpiration
uuid: 19b37bd4-f7cf-4b5f-be1a-b2d9fda5b4b1
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# NonImgExpiration{#nonimgexpiration}

TTL do cache do cliente para respostas que não sejam de imagem. Fornece o intervalo de expiração para determinadas respostas que não são de imagem.

Fornece o intervalo de expiração para determinadas respostas que não são de imagem, incluindo as enviadas em resposta aos seguintes comandos:

* `req=imageset`
* `req=catalogprops`
* `req=exists`
* `req=imageprops`
* `req=props`

## Propriedades {#section-d37e3113f4b1468b86b5a14e80d94c83}

Número real, 0 ou superior. Número de horas até a expiração desde que os dados de resposta foram gerados. Defina como 0 para sempre expirar a imagem de resposta imediatamente, o que efetivamente desativa o armazenamento em cache do cliente para respostas de imagem padrão. Defina como -1 para marcar como *nunca expira*.

## Padrão {#section-96981360c0234b7f824d2ff7c25a7954}

Herdado de `default::NonImgExpiration` se não estiver definido ou se estiver vazio.

TTL (Time-To-Live) é a duração antes do cache expirar. O TTL padrão é de 6 minutos.

## Consulte também {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
