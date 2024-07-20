---
description: Resolução. Resolução de imagem "real", normalmente expressa em pixels por polegada, mas também pode estar em outras unidades, como pixels por metro.
solution: Experience Manager
title: Resolução
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 45b12324-3148-4530-82cd-0ee32e9f98f8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 0%

---

# Resolução{#resolution}

Resolução. Resolução de imagem &quot;real&quot;, normalmente expressa em pixels por polegada, mas também pode estar em outras unidades, como pixels por metro.

## Propriedades {#section-985ca2ad858c4e9c9cbb303f55447553}

Número real, maior que 0. Necessário para materiais de textura e decalque, a menos que a resolução da imagem seja a mesma que attribute::Resolution. Ignorado por materiais de gabinete e cores sólidas.

## Padrão {#section-b1d044e211194242a900aaef4a8c8e6f}

`attribute::Resolution` é usado se o campo não estiver presente, se o valor for 0 ou negativo, ou se o campo estiver vazio.

## Consulte também {#section-2d04df523d7345f6929178cbc637da78}

[atributo::Resolução](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-09fe14e6bfbf4db6b7f4369fffecc806) , [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04)
