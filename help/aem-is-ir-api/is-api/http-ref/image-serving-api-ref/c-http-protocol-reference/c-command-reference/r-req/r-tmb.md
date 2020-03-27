---
description: Imagem em miniatura. Solicita dados de imagem formatados e dimensionados usando critérios de miniatura do catálogo.
seo-description: Imagem em miniatura. Solicita dados de imagem formatados e dimensionados usando critérios de miniatura do catálogo.
seo-title: tmb
solution: Experience Manager
title: tmb
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f098c30-a164-47a6-abb2-0eb1d0bc24da
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# tmb{#tmb}

Imagem em miniatura. Solicita dados de imagem formatados e dimensionados usando critérios de miniatura do catálogo.

`req=tmb`

O formato de dados de resposta e o tipo MIME de resposta são determinados por `fmt=`. Suporta todos os comandos, exceto `fit=`.

Consulte Escala de [miniaturas](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::Expiration`.
