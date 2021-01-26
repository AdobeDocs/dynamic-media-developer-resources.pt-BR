---
description: Perfil de cores de saída padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta RGB quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor RGB especificados com vários comandos de Renderização de imagem, como bgc= e color=.
seo-description: Perfil de cores de saída padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta RGB quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor RGB especificados com vários comandos de Renderização de imagem, como bgc= e color=.
seo-title: IccProfileRgb
solution: Experience Manager
title: IccProfileRgb
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0fe63607-c328-468a-aa55-0c4d16cf9f0f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---


# IccProfileRgb{#iccprofilergb}

Perfil de cores de saída padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta RGB quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor RGB especificados com vários comandos de Renderização de imagem, como bgc= e color=.

## Propriedades {#section-b4a1bd92e99047479a5036413525a6d9}

Sequência de caracteres de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfis ICC desse catálogo de materiais ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil RGB.

## Padrão {#section-5809772f8e96438ab7626d323c66a4ba}

Herdado de `default::IccProfileRgb` se não estiver definido ou se estiver vazio.

## Consulte também {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [atributo::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49),  [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
