---
title: IccProfileGray
description: Perfil de cor de saída padrão em tons de cinza. Especifica o nome do perfil de cores ICC a ser usado para imagens de resposta em tons de cinza quando nenhum espaço de cores de saída for especificado com icc= e para determinados valores de cores em tons de cinza especificados com vários comandos do Servidor de imagens, como color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# IccProfileGray{#iccprofilegray}

Perfil de cor de saída padrão em tons de cinza. Especifica o nome do perfil de cores ICC a ser usado para imagens de resposta em tons de cinza quando nenhum espaço de cores de saída for especificado com icc= e para determinados valores de cores em tons de cinza especificados com vários comandos do Servidor de imagens, como color=.

## Propriedades {#section-03f090ee2acf4537b83f78840d23ecab}

String de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfis ICC deste catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil em tons de cinza.

## Padrão {#section-95ba3ab15edc4259b657c6ebf8783d61}

Herdado de `default::IccProfileGray` se não estiver definido ou se estiver vazio.

## Consulte também {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
