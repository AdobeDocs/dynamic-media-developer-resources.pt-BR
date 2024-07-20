---
title: Expiração
description: Tempo de vida padrão do cache do cliente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Expiração{#expiration}

Tempo de vida padrão do cache do cliente. Fornece um intervalo de expiração padrão caso um determinado registro de catálogo não contenha um valor de `catalog::Expiration` ou `vignette::Expiration` válido. Ou, se um arquivo de vinheta ou de material for acessado diretamente, não por meio de um registro de catálogo.

## Propriedades {#section-8e2bade105ec4905ae5c4911f500279f}

Número real, `0` ou maior. Número de horas até a expiração desde que os dados de resposta foram gerados. Defina como `0` para sempre expirar a imagem de resposta imediatamente, o que desabilita efetivamente o cache do cliente. Defina como `-1` para marcar como *nunca expirará*.

## Padrão {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Herdado de `default::Expiration` se não estiver definido ou se estiver vazio.

## Consulte também {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catálogo::Expiração](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) , [vinheta::Expiração](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
