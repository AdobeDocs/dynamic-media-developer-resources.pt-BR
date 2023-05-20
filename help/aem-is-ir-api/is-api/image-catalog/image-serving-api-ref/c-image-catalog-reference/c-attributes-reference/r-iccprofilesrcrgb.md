---
description: perfil de cor de entrada padrão do RGB. Especifica o nome do perfil de cores ICC a ser usado para imagens de origem de RGB que não incorporam um perfil de cores e para determinados valores de cores de RGB especificados com vários comandos do Servidor de imagens, como color=.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfcbd9fe-e696-46e3-abbf-497dc55fe855
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

perfil de cor de entrada padrão do RGB. Especifica o nome do perfil de cores ICC a ser usado para imagens de origem de RGB que não incorporam um perfil de cores e para determinados valores de cores de RGB especificados com vários comandos do Servidor de imagens, como color=.

## Propriedades {#section-3cd753196959462e9e674dab0b033d08}

String de texto. Se especificado, deve ser um válido `icc::Name` valor do mapa de perfis ICC deste catálogo de imagens, do catálogo padrão ou de um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil RGB.

## Padrão {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Herdado de `default::IccProfileSrcRgb` se não estiver definido ou se estiver vazio. Se `attribute::IccProfileSrcRgb` não resolve um perfil válido, `attribute::IccProfileRgb` é usado em seu lugar.

## Consulte também {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
