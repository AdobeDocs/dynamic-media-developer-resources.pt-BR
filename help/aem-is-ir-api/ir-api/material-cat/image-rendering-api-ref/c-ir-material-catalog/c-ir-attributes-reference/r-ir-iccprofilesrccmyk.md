---
description: PERFIL de cor de entrada padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de material CMYK que não incorporam um perfil de cor.
seo-description: PERFIL de cor de entrada padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de material CMYK que não incorporam um perfil de cor.
seo-title: IccProfileSrcCmyk
solution: Experience Manager
title: IccProfileSrcCmyk
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 95147b28-c87b-4337-a0eb-a962ca1e8786
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# IccProfileSrcCmyk{#iccprofilesrccmyk}

PERFIL de cor de entrada padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de material CMYK que não incorporam um perfil de cor.

## Propriedades {#section-0cee77438d914c319ec876edb3490821}

Sequência de caracteres de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfis ICC desse catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil CMYK.

## Padrão {#section-11f6239e0dd14827abf4a95c1b30161c}

Herdado de `default::IccProfileSrcCmyk` se não estiver definido ou se estiver vazio. Se `attribute::IccProfileSrcCmyk` não for resolvido para um perfil válido, `attribute::IccProfileCmyk` será usado.

## Consulte também {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [atributo::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127),  [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
