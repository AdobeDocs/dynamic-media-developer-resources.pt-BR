---
description: Tempo de funcionamento do cache do cliente. Número de horas até a expiração. Usado para gerenciar o armazenamento em cache do cliente e do servidor proxy.
solution: Experience Manager
title: Expiração
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 0%

---

# Expiração{#expiration}

Tempo de funcionamento do cache do cliente. Número de horas até a expiração. Usado para gerenciar o armazenamento em cache do cliente e do servidor proxy.

Consulte ` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)` para obter detalhes.

## Propriedades {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Número real, -2, -1, 0 ou maior. Número de horas até a expiração desde que a imagem de resposta foi gerada. Defina como 0 para sempre expirar a imagem de resposta imediatamente, o que efetivamente desativa o armazenamento em cache do cliente. Defina como -1 para marcar como `never expire`; nesse caso, o servidor sempre retorna o status 403 em resposta a solicitações condicionais `GET` sem verificar se o arquivo foi realmente alterado. Defina como -2 para usar o padrão fornecido por `attribute::Expiration`.

## Padrão {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` é usado se o campo não estiver presente, se o valor for -2 ou se o campo estiver vazio.

## Consulte também {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[atributo::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
