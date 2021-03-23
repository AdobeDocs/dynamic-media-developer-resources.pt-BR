---
description: TTL do cache do cliente para respostas de imagem padrão. Fornece o intervalo de expiração para respostas de imagem padrão (respostas que retornam uma imagem padrão especificada com defaultImage= ou atributo DefaultImage).
seo-description: TTL do cache do cliente para respostas de imagem padrão. Fornece o intervalo de expiração para respostas de imagem padrão (respostas que retornam uma imagem padrão especificada com defaultImage= ou atributo DefaultImage).
seo-title: DefaultExpiration
solution: Experience Manager
title: DefaultExpiration
uuid: 5266bff9-f20b-4b3b-9566-8a3f5ba0777a
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 0%

---


# DefaultExpiration{#defaultexpiration}

TTL do cache do cliente para respostas de imagem padrão. Fornece o intervalo de expiração para respostas de imagem padrão (respostas que retornam uma imagem padrão especificada com defaultImage= ou attribute::DefaultImage).

Aplicado somente quando a imagem padrão não está associada a um registro de catálogo ou quando o registro de catálogo de imagem padrão não fornece um valor `catalog::Expiration` específico.

## Propriedades {#section-e564512476604fd7b964f9f2903d6d33}

Número real, 0 ou superior. Número de horas até a expiração desde que os dados de resposta foram gerados. Defina como 0 para sempre expirar a imagem de resposta imediatamente, o que efetivamente desativa o armazenamento em cache do cliente para respostas de imagem padrão. Defina como `-1` para marcar como `never expire`.

## Padrão {#section-131cd32c2e214391857dba5af321f8cd}

Herdado de `default::DefaultExpiration` se não estiver definido ou se estiver vazio.

TTL (Time-To-Live) é a duração antes do cache expirar. O TTL padrão é de 1 hora.

## Consulte também {#section-d8642c22e3d947129367dd76366963d6}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
