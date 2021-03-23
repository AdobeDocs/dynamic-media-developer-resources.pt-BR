---
description: Perfil de cor de entrada padrão de escala de cinza. Especifica o nome do perfil de cor ICC a ser usado para imagens de origem em tons de cinza que não incorporam um perfil de cor e para determinados valores de cor em escala de cinza especificados com vários comandos de Exibição de imagem, como color=.
seo-description: Perfil de cor de entrada padrão de escala de cinza. Especifica o nome do perfil de cor ICC a ser usado para imagens de origem em tons de cinza que não incorporam um perfil de cor e para determinados valores de cor em escala de cinza especificados com vários comandos de Exibição de imagem, como color=.
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
uuid: 823c0e33-8bb7-4754-81cf-61a5ed6f45ce
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---


# IccProfileSrcGray{#iccprofilesrcgray}

Perfil de cor de entrada padrão de escala de cinza. Especifica o nome do perfil de cor ICC a ser usado para imagens de origem em tons de cinza que não incorporam um perfil de cor e para determinados valores de cor em escala de cinza especificados com vários comandos de Exibição de imagem, como color=.

## Propriedades {#section-8cbb316df6eb463aaca7b308d3568086}

Sequência de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfil ICC deste catálogo de imagem ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil em tons de cinza.

## Padrão {#section-bcc7250715884412bd0780f60d1cce7b}

Herdado de `default::IccProfileSrcGray` se não estiver definido ou se estiver vazio. Se `attribute::IccProfileSrcGray` não for resolvido para um perfil válido, `attribute::IccProfileGray` será usado.

## Consulte também {#section-e429b76daf2e4b92b326db2b0bcbd0c5}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilegray.md#reference-13822a1596e440eea0492e86d88dad35),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
