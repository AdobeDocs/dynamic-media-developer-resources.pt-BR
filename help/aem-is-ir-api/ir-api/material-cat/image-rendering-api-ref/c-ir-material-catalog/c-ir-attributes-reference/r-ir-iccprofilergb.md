---
title: IccProfileRgb
description: perfil de cores de saída padrão do RGB. Especifica o nome do perfil de cores ICC a ser usado para imagens de resposta de RGB quando nenhum espaço de cores de saída for especificado com icc=. Também para determinados valores de cor de RGB especificados com vários comandos de Renderização de imagem, como bgc= e color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4057e968-24de-41af-9901-a6cb5ed9ea63
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# IccProfileRgb{#iccprofilergb}

perfil de cores de saída padrão do RGB. Especifica o nome do perfil de cores ICC a ser usado para imagens de resposta de RGB quando nenhum espaço de cores de saída for especificado com `icc=`. Também para determinados valores de cor de RGB especificados com vários comandos de Renderização de Imagem, como `bgc=` e `color=`.

## Propriedades {#section-b4a1bd92e99047479a5036413525a6d9}

String de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfis ICC deste catálogo de materiais ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil RGB.

## Padrão {#section-5809772f8e96438ab7626d323c66a4ba}

Herdado de `default::IccProfileRgb` se não estiver definido ou se estiver vazio.

## Consulte também {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) , [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attribute::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
