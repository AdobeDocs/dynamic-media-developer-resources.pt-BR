---
description: Perfil de cores de saída padrão do RGB. Especifica o nome do perfil de cores ICC a ser usado para imagens de resposta do RGB quando nenhum espaço de cores de saída for especificado com icc= e para determinados valores de cores do RGB especificados com vários comandos do Servidor de imagens, como color=.
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 861c7b54-6d18-47c8-a08d-970f29b63962
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# IccProfileRgb{#iccprofilergb}

Perfil de cores de saída padrão do RGB. Especifica o nome do perfil de cores ICC a ser usado para imagens de resposta do RGB quando nenhum espaço de cores de saída for especificado com icc= e para determinados valores de cores do RGB especificados com vários comandos do Servidor de imagens, como color=.

## Propriedades {#section-3dd55c954d4d4ad4bb715ed7cee31025}

String de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfis ICC deste catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil RGB.

## Padrão {#section-dfe08dd7b851453ca816623a4179955b}

Herdado de `default::IccProfileRgb` se não estiver definido ou se estiver vazio.

## Consulte também {#section-05bc25ab7caa418ca94d43ced905add7}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcrgb.md#reference-b8e576d075b44f5c94d95bfb5aa22ae2), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
