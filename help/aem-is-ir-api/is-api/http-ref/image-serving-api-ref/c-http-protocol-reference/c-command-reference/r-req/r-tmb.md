---
description: Imagem em miniatura. Solicita dados de imagem formatados e dimensionados usando critérios de miniatura de catálogo.
seo-description: Imagem em miniatura. Solicita dados de imagem formatados e dimensionados usando critérios de miniatura de catálogo.
seo-title: tmb
solution: Experience Manager
title: tmb
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---


# tmb{#tmb}

Imagem em miniatura. Solicita dados de imagem formatados e dimensionados usando critérios de miniatura de catálogo.

`req=tmb`

O formato dos dados de resposta e o tipo MIME de resposta são determinados por `fmt=`. Suporta todos os comandos, exceto `fit=`.

Consulte [Escala de miniaturas](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

A resposta HTTP pode ser armazenada em cache com o TTL com base em `catalog::Expiration`.
