---
description: Perfil de cores de entrada padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de material RGB e vinhetas que não incorporam um perfil de cor e para valores de cor RGB especificados com vários comandos de Renderização de imagem, como bgc= e color=.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 1c90c77c-79b7-41aa-9269-b48d966ba362
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

Perfil de cores de entrada padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de material RGB e vinhetas que não incorporam um perfil de cor e para valores de cor RGB especificados com vários comandos de Renderização de imagem, como bgc= e color=.

## Propriedades {#section-c22966bba03e43c08e9d3fb91bfdd465}

Sequência de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfil ICC deste catálogo de imagem ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil RGB.

## Padrão {#section-0171cd6680284bfa9844b9cc3644ca61}

Herdado de `default::IccProfileSrcRgb` se não estiver definido ou se estiver vazio. Se `attribute::IccProfileSrcRgb` não for resolvido para um perfil válido, `attribute::IccProfileRgb` será usado.

## Consulte também {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
