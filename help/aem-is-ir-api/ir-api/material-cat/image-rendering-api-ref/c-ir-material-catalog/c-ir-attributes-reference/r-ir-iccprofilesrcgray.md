---
description: Perfil de cor de entrada padrão de escala de cinza. Especifica o nome do perfil de cor ICC a ser usado para imagens de materiais em tons de cinza que não incorporam um perfil de cor.
solution: Experience Manager
title: IccProfileSrcGray
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8c89f0bb-4912-4838-a9e2-fb5d2f255eae
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# IccProfileSrcGray{#iccprofilesrcgray}

Perfil de cor de entrada padrão de escala de cinza. Especifica o nome do perfil de cor ICC a ser usado para imagens de materiais em tons de cinza que não incorporam um perfil de cor.

## Propriedades {#section-97923d8561b845309442d57d017d91a4}

Sequência de texto. Se especificado, deve ser válido `icc::Name` valor do mapa de perfil ICC deste catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil em tons de cinza.

## Padrão {#section-02c52805ee13483dba7878aeab51f889}

Herdado de `default::IccProfileSrcGray` se não estiver definido ou se estiver vazio. If `attribute::IccProfileSrcGray` não resolve para um perfil válido, `attribute::IccProfileGray` é usada em vez disso.

## Consulte também {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [atributo::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6), [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
