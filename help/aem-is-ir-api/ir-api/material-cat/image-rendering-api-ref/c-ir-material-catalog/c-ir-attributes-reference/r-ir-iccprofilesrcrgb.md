---
description: Perfil de cores de entrada padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de material RGB e vinhetas que não incorporam um perfil de cor e para valores de cor RGB especificados com vários comandos de Renderização de imagem, como bgc= e color=.
seo-description: Perfil de cores de entrada padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de material RGB e vinhetas que não incorporam um perfil de cor e para valores de cor RGB especificados com vários comandos de Renderização de imagem, como bgc= e color=.
seo-title: IccProfileSrcRgb
solution: Experience Manager
title: IccProfileSrcRgb
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9657e296-0d2a-4b05-9be7-5a54d3277f90
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# IccProfileSrcRgb{#iccprofilesrcrgb}

Perfil de cores de entrada padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de material RGB e vinhetas que não incorporam um perfil de cor e para valores de cor RGB especificados com vários comandos de Renderização de imagem, como bgc= e color=.

## Propriedades {#section-c22966bba03e43c08e9d3fb91bfdd465}

Sequência de caracteres de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfis ICC desse catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil RGB.

## Padrão {#section-0171cd6680284bfa9844b9cc3644ca61}

Herdado de `default::IccProfileSrcRgb` se não estiver definido ou se estiver vazio. Se `attribute::IccProfileSrcRgb` não for resolvido para um perfil válido, `attribute::IccProfileRgb` será usado.

## Consulte também {#section-1ba91666830f4c209c39260ea29f938e}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [atributo::IccProfileRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilergb.md#reference-cdaad25b155646ffa382d722fd324b30),  [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
