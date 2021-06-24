---
description: Perfil de cor de saída padrão de escala de cinza. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta em tons de cinza quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor em escala de cinza especificados com vários comandos do Image Serving, como color=.
solution: Experience Manager
title: IccProfileGray
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---

# IccProfileGray{#iccprofilegray}

Perfil de cor de saída padrão de escala de cinza. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta em tons de cinza quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor em escala de cinza especificados com vários comandos do Image Serving, como color=.

## Propriedades {#section-03f090ee2acf4537b83f78840d23ecab}

Sequência de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfil ICC deste catálogo de imagem ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil em tons de cinza.

## Padrão {#section-95ba3ab15edc4259b657c6ebf8783d61}

Herdado de `default::IccProfileGray` se não estiver definido ou se estiver vazio.

## Consulte também {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) ,  [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9),  [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
