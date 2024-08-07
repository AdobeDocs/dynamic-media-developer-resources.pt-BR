---
title: IccProfileSrcGray
description: Perfil de cor de entrada padrão em escala de cinza. Especifica o nome do perfil de cores ICC a ser usado para imagens de material em tons de cinza que não incorporam um perfil de cores.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8c89f0bb-4912-4838-a9e2-fb5d2f255eae
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# IccProfileSrcGray{#iccprofilesrcgray}

Perfil de cor de entrada padrão em escala de cinza. Especifica o nome do perfil de cores ICC a ser usado para imagens de material em tons de cinza que não incorporam um perfil de cores.

## Propriedades {#section-97923d8561b845309442d57d017d91a4}

String de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfis ICC deste catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil em tons de cinza.

## Padrão {#section-02c52805ee13483dba7878aeab51f889}

Herdado de `default::IccProfileSrcGray` se não estiver definido ou se estiver vazio. Se `attribute::IccProfileSrcGray` não for resolvido para um perfil válido, `attribute::IccProfileGray` será usado.

## Consulte também {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
