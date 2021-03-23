---
description: Perfil de cores de entrada padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de origem CMYK que não incorporam um perfil de cor e para determinados valores de cor CMYK especificados com vários comandos de Exibição de imagem, como color=.
seo-description: Perfil de cores de entrada padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de origem CMYK que não incorporam um perfil de cor e para determinados valores de cor CMYK especificados com vários comandos de Exibição de imagem, como color=.
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
uuid: 5f1c2eb6-7f32-4603-9587-d8c1f6a72bb0
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

Perfil de cores de entrada padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de origem CMYK que não incorporam um perfil de cor e para determinados valores de cor CMYK especificados com vários comandos de Exibição de imagem, como color=.

## Propriedades {#section-fc2ad12a3c6e4c7cab495f1878638e66}

Sequência de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfil ICC deste catálogo de imagem ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil CMYK.

## Padrão {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Herdado de `default::IccProfileSrcCmyk` se não estiver definido ou se estiver vazio. Se `attribute::IccProfileSrcCmyk` não for resolvido para um perfil válido, `attribute::IccProfileCmyk` será usado.

## Consulte também {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
