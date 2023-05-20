---
title: IccProfileSrcCmyk
description: Perfil de cor de entrada padrão CMYK. Especifica o nome do perfil de cores ICC a ser usado para imagens de material CMYK que não incorporam um perfil de cores.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 09be34c8-facc-40c3-ba15-c48bd93b3be1
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# IccProfileSrcCmyk{#iccprofilesrccmyk}

Perfil de cor de entrada padrão CMYK. Especifica o nome do perfil de cores ICC a ser usado para imagens de material CMYK que não incorporam um perfil de cores.

## Propriedades {#section-0cee77438d914c319ec876edb3490821}

String de texto. Se especificado, deve ser um válido `icc::Name` valor do mapa de perfis ICC deste catálogo de imagens, do catálogo padrão ou de um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil CMYK.

## Padrão {#section-11f6239e0dd14827abf4a95c1b30161c}

Herdado de `default::IccProfileSrcCmyk` se não estiver definido ou se estiver vazio. Se `attribute::IccProfileSrcCmyk` não resolve um perfil válido, `attribute::IccProfileCmyk` é usado em seu lugar.

## Consulte também {#section-88adddd70265459a9a5d2f50829a4ba7}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
