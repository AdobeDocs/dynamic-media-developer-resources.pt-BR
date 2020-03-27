---
description: perfil de cor de saída padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta CMYK quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor CMYK especificados com vários comandos do Servidor de imagens, como color=.
seo-description: perfil de cor de saída padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta CMYK quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor CMYK especificados com vários comandos do Servidor de imagens, como color=.
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
topic: Scene7 Image Serving - Image Rendering API
uuid: b22b6ed1-615f-4241-b4d4-c3aa70351458
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileCmyk{#iccprofilecmyk}

perfil de cor de saída padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta CMYK quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor CMYK especificados com vários comandos do Servidor de imagens, como color=.

## Propriedades {#section-d8b6102cc1c744d482f99808ccfcaa24}

Sequência de caracteres de texto. Se especificado, deve ser um `icc::Name` valor válido do mapa de perfis ICC desse catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil CMYK.

## Padrão {#section-62442df09a724950bfbdd0640b3e6678}

Herdado de `default::IccProfileCmyk` se não estiver definido ou se estiver vazio.

## Consulte também {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [atributo::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728), [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
