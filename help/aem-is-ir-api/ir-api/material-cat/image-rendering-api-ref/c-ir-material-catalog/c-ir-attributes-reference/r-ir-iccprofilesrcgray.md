---
description: Perfil de cor de entrada padrão em tons de cinza. Especifica o nome do perfil de cor ICC a ser usado para imagens de material em tons de cinza que não incorporam um perfil de cor.
seo-description: Perfil de cor de entrada padrão em tons de cinza. Especifica o nome do perfil de cor ICC a ser usado para imagens de material em tons de cinza que não incorporam um perfil de cor.
seo-title: IccProfileSrcGray
solution: Experience Manager
title: IccProfileSrcGray
topic: Scene7 Image Serving - Image Rendering API
uuid: e05d1185-ffd6-4c04-a2b8-52228beae37d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# IccProfileSrcGray{#iccprofilesrcgray}

Perfil de cor de entrada padrão em tons de cinza. Especifica o nome do perfil de cor ICC a ser usado para imagens de material em tons de cinza que não incorporam um perfil de cor.

## Propriedades {#section-97923d8561b845309442d57d017d91a4}

Sequência de caracteres de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfis ICC desse catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil em tons de cinza.

## Padrão {#section-02c52805ee13483dba7878aeab51f889}

Herdado de `default::IccProfileSrcGray` se não estiver definido ou se estiver vazio. Se `attribute::IccProfileSrcGray` não for resolvido para um perfil válido, `attribute::IccProfileGray` será usado.

## Consulte também {#section-c361d6f6231942b3aa8b4b496e1d3de3}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [atributo::IccProfileGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilegray.md#reference-712f1d0dcca748df9aaf495681bb39e6),  [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
