---
description: TTL de cache do cliente para respostas de imagem padrão. Fornece o intervalo de expiração para respostas de imagem padrão (respostas que retornam uma imagem padrão especificada com defaultImage= ou o atributo DefaultImage).
solution: Experience Manager
title: DefaultExpiration
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 99103681-c00c-4648-8dee-2314e7e614af
TQID: 'https://experienceleague.adobe.com/v-wtXCBtpHpf9mTjoQ58GZ9eXq-yR2tpGT0Kd-DTyNI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 0%

---

# DefaultExpiration{#defaultexpiration}

TTL de cache do cliente para respostas de imagem padrão. Fornece o intervalo de expiração para respostas de imagem padrão (respostas que retornam uma imagem padrão especificada com defaultImage= ou attribute::DefaultImage).

Aplicado somente quando a imagem padrão não está associada a um registro de catálogo ou quando o registro de catálogo de imagens padrão não fornece um valor `catalog::Expiration` específico.

## Propriedades {#section-e564512476604fd7b964f9f2903d6d33}

Número real, 0 ou maior. Número de horas até a expiração desde que os dados de resposta foram gerados. Defina como 0 para sempre expirar a imagem de resposta imediatamente, o que desativa efetivamente o cache do cliente para respostas de imagem padrão. Defina como `-1` para marcar como `never expire`.

## Padrão {#section-131cd32c2e214391857dba5af321f8cd}

Herdado de `default::DefaultExpiration` se não estiver definido ou se estiver vazio.

TTL (Time-To-Live) é a duração antes do cache expirar. O TTL padrão é 1 hora.

## Consulte também {#section-d8642c22e3d947129367dd76366963d6}

[catálogo::Expiração](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-svg-data-reference/r-expiration-svg.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [atributo::ImagemPadrão](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433)
