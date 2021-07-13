---
description: Tempo de vida padrão do cache do cliente. Fornece um intervalo de expiração padrão no caso de um registro de catálogo específico não conter um valor válido de Expiração de catálogo ou de expiração de vinheta, ou se um arquivo de vinheta ou arquivo de material for acessado diretamente, em vez de por um registro de catálogo.
solution: Experience Manager
title: Expiração
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 6d9cca06-f675-4ae4-a187-9cd716e7c554
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Expiração{#expiration}

Tempo de vida padrão do cache do cliente. Fornece um intervalo de expiração padrão no caso de um registro de catálogo específico não conter um catálogo válido::Expiration or vinnette::Expiration value ou se um arquivo de vinheta ou arquivo de material for acessado diretamente, em vez de por um registro de catálogo.

## Propriedades {#section-8e2bade105ec4905ae5c4911f500279f}

Número real, 0 ou superior. Número de horas até a expiração desde que os dados de resposta foram gerados. Defina como 0 para sempre expirar a imagem de resposta imediatamente, o que efetivamente desativa o armazenamento em cache do cliente. Defina como -1 para marcar como *nunca expira*.

## Padrão {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Herdado do padrão::Expiration se não estiver definido ou se estiver vazio.

## Consulte também {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ,  [vinheta::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
