---
description: perfil de cores de saída padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta RGB quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor RGB especificados com vários comandos do Servidor de imagens, como color=.
seo-description: perfil de cores de saída padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta RGB quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor RGB especificados com vários comandos do Servidor de imagens, como color=.
seo-title: IccProfileRgb
solution: Experience Manager
title: IccProfileRgb
topic: Scene7 Image Serving - Image Rendering API
uuid: 40606151-d5fa-4ae5-b6f0-e811bfea4691
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# IccProfileRgb{#iccprofilergb}

perfil de cores de saída padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta RGB quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor RGB especificados com vários comandos do Servidor de imagens, como color=.

## Propriedades {#section-3dd55c954d4d4ad4bb715ed7cee31025}

Sequência de caracteres de texto. Se especificado, deve ser um `icc::Name` valor válido do mapa de perfis ICC desse catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil RGB.

## Padrão {#section-dfe08dd7b851453ca816623a4179955b}

Herdado de `default::IccProfileRgb` se não estiver definido ou se estiver vazio.

## Consulte também {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [atributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [atributo::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2), [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
