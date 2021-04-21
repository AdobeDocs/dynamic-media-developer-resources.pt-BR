---
description: Perfil de cor de saída padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta CMYK quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor CMYK especificados com vários comandos do Image Serving, como color=.
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---


# IccProfileCmyk{#iccprofilecmyk}

Perfil de cor de saída padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta CMYK quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor CMYK especificados com vários comandos do Image Serving, como color=.

## Propriedades {#section-d8b6102cc1c744d482f99808ccfcaa24}

Sequência de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfil ICC deste catálogo de imagem ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil CMYK.

## Padrão {#section-62442df09a724950bfbdd0640b3e6678}

Herdado de `default::IccProfileCmyk` se não estiver definido ou se estiver vazio.

## Consulte também {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
