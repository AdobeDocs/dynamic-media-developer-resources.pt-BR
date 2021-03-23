---
description: Perfil de cores de entrada padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de origem RGB que não incorporam um perfil de cor e para determinados valores de cor RGB especificados com vários comandos de Exibição de imagem, como color=.
seo-description: Perfil de cores de entrada padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de origem RGB que não incorporam um perfil de cor e para determinados valores de cor RGB especificados com vários comandos de Exibição de imagem, como color=.
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
uuid: 4f6f19ec-3524-403e-9c79-1e2b25cd74ce
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

Perfil de cores de entrada padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de origem RGB que não incorporam um perfil de cor e para determinados valores de cor RGB especificados com vários comandos de Exibição de imagem, como color=.

## Propriedades {#section-3cd753196959462e9e674dab0b033d08}

Sequência de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfil ICC deste catálogo de imagem ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil RGB.

## Padrão {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Herdado de `default::IccProfileSrcRgb` se não estiver definido ou se estiver vazio. Se `attribute::IccProfileSrcRgb` não for resolvido para um perfil válido, `attribute::IccProfileRgb` será usado.

## Consulte também {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
