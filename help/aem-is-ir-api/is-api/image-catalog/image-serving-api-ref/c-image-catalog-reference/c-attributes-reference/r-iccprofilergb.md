---
description: Perfil de cores de saída padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta RGB quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor RGB especificados com vários comandos de Exibição de imagem, como color=.
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# IccProfileRgb{#iccprofilergb}

Perfil de cores de saída padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta RGB quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor RGB especificados com vários comandos de Exibição de imagem, como color=.

## Propriedades {#section-3dd55c954d4d4ad4bb715ed7cee31025}

Sequência de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfil ICC deste catálogo de imagem ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil RGB.

## Padrão {#section-dfe08dd7b851453ca816623a4179955b}

Herdado de `default::IccProfileRgb` se não estiver definido ou se estiver vazio.

## Consulte também {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
