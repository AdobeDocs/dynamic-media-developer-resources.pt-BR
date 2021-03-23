---
description: Tempo de vida padrão do cache do cliente. Fornece um intervalo de expiração padrão no caso de um registro de catálogo específico não conter um valor válido de Expiração de catálogo ou de expiração de vinheta, ou se um arquivo de vinheta ou arquivo de material for acessado diretamente, em vez de por um registro de catálogo.
seo-description: Tempo de vida padrão do cache do cliente. Fornece um intervalo de expiração padrão no caso de um registro de catálogo específico não conter um valor válido de Expiração de catálogo ou de expiração de vinheta, ou se um arquivo de vinheta ou arquivo de material for acessado diretamente, em vez de por um registro de catálogo.
seo-title: Expiração
solution: Experience Manager
title: Expiração
uuid: 2b56f9ec-2b25-4e6a-aead-6dad3d2df975
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---


# Expiração{#expiration}

Tempo de vida padrão do cache do cliente. Fornece um intervalo de expiração padrão no caso de um registro de catálogo específico não conter um catálogo válido::Expiration ou vinheta::Expiration value ou se um arquivo de vinheta ou arquivo de material for acessado diretamente, em vez de por um registro de catálogo.

## Propriedades {#section-8e2bade105ec4905ae5c4911f500279f}

Número real, 0 ou superior. Número de horas até a expiração desde que os dados de resposta foram gerados. Defina como 0 para sempre expirar a imagem de resposta imediatamente, o que efetivamente desativa o armazenamento em cache do cliente. Defina como -1 para marcar como *nunca expira*.

## Padrão {#section-18cfce46edb441bfae7dd9d3e0217ba9}

Herdado do padrão::Expiration se não estiver definido ou se estiver vazio.

## Consulte também {#section-ecfe21ff789c4b298344ebf7c647b7e7}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce) ,  [vinheta::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c)
