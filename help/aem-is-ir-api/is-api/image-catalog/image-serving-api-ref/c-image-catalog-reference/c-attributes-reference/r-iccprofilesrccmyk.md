---
title: IccProfileSrcCmyk
description: Perfil de cor de entrada padrão CMYK. Especifica o nome do perfil de cores ICC a ser usado para imagens de origem CMYK que não incorporam um perfil de cores e para determinados valores de cores CMYK especificados com vários comandos do Servidor de imagens, como color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 018170f3-2d1a-4da1-a480-b0a7e19457d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

Perfil de cor de entrada padrão CMYK. Especifica o nome do perfil de cores ICC a ser usado para imagens de origem CMYK que não incorporam um perfil de cores e para determinados valores de cores CMYK especificados com vários comandos do Servidor de imagens, como color=.

## Propriedades {#section-fc2ad12a3c6e4c7cab495f1878638e66}

String de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfis ICC deste catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil CMYK.

## Padrão {#section-c1f63b4bd32a4f38bf5d68decb9e25da}

Herdado de `default::IccProfileSrcCmyk` se não estiver definido ou se estiver vazio. Se `attribute::IccProfileSrcCmyk` não for resolvido para um perfil válido, `attribute::IccProfileCmyk` será usado.

## Consulte também {#section-a6623bd4277e43b084ec0fb9e02069dc}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
