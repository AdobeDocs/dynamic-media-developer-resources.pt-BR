---
description: Resolução de miniaturas. Especifica a resolução do objeto para a imagem em miniatura.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 1b462b7e-076d-433e-a5d2-e254396c4659
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# ThumbRes{#thumbres}

Resolução de miniaturas. Especifica a resolução do objeto para a imagem em miniatura.

Usado somente se `catalog::ThumbType=3`.

## Propriedades {#section-ee5cae086a3d4875805fa8a08756a586}

Valor do número real maior que 0. Deve ter as mesmas unidades que `catalog::Resolution`.

## Padrão {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` é usado se o campo não estiver presente, se o valor for 0 ou se o campo estiver vazio.

## Consulte também {#section-eb716bf647614db083020fe8ce453751}

[catalog:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) ,  [catalog::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1),  [atributo::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501),  [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76),  [Thumbnail Scaling](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
