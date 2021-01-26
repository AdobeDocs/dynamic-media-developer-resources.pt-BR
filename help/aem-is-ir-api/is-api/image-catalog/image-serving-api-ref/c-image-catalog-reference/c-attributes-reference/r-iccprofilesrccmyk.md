---
description: PERFIL de cor de entrada padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de origem CMYK que não incorporam um perfil de cor e para determinados valores de cor CMYK especificados com vários comandos do Servidor de imagens, como color=.
seo-description: PERFIL de cor de entrada padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de origem CMYK que não incorporam um perfil de cor e para determinados valores de cor CMYK especificados com vários comandos do Servidor de imagens, como color=.
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5f1c2eb6-7f32-4603-9587-d8c1f6a72bb0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

PERFIL de cor de entrada padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de origem CMYK que não incorporam um perfil de cor e para determinados valores de cor CMYK especificados com vários comandos do Servidor de imagens, como color=.

## Propriedades {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Sequência de caracteres de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfis ICC desse catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil CMYK.

## Padrão {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Herdado de `default::IccProfileSrcCmyk` se não estiver definido ou se estiver vazio. Se `attribute::IccProfileSrcCmyk` não for resolvido para um perfil válido, `attribute::IccProfileCmyk` será usado.

## Consulte também {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [atributo::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0),  [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
