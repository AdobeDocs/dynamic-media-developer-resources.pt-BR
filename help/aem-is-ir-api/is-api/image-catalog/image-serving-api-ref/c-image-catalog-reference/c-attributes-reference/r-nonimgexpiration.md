---
description: TTL de cache do cliente para respostas que não são de imagem. Fornece o intervalo de expiração para determinadas respostas que não sejam de imagem.
solution: Experience Manager
title: NonImgExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c61e2781-dfaa-4f3d-958d-5ffa755a3e4d
TQID: 'https://experienceleague.adobe.com/A21KkwsYFIMp9Pw0WyX-c-3UVlFg2FacObh2jjRVTwA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 128
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

Número real, 0 ou maior. Número de horas até a expiração desde que os dados de resposta foram gerados. Defina como 0 para sempre expirar a imagem de resposta imediatamente, o que desativa efetivamente o cache do cliente para respostas de imagem padrão. Defina como -1 para marcar como *nunca expirará*.

## Padrão {#section-96981360c0234b7f824d2ff7c25a7954}

Herdado de `default::NonImgExpiration` se não estiver definido ou se estiver vazio.

TTL (Time-To-Live) é a duração antes do cache expirar. O TTL padrão é de 6 minutos.

## Consulte também {#section-4549c5594a5547beb8b129ec8d0e6aa6}

[catálogo::Expiração](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [atributo::ImagemPadrão](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
