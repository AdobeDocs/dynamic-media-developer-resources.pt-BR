---
description: Imagem em miniatura. Solicita dados de imagem formatados e dimensionados usando critérios de miniatura de catálogo.
solution: Experience Manager
title: tmb
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 9bdcc1c4-fe2b-4316-a472-07a533f105a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---

# tmb{#tmb}

Imagem em miniatura. Solicita dados de imagem formatados e dimensionados usando critérios de miniatura de catálogo.

`req=tmb`

O formato dos dados de resposta e o tipo MIME de resposta são determinados por `fmt=`. Suporta todos os comandos, exceto `fit=`.

Consulte [Escala de miniaturas](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f).

A resposta HTTP pode ser armazenada em cache com o TTL com base em `catalog::Expiration`.
