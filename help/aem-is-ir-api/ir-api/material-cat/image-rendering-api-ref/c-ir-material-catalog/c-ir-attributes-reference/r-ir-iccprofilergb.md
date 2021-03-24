---
description: Perfil de cores de saída padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta RGB quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor RGB especificados com vários comandos de renderização de imagem, como bgc= e color=.
solution: Experience Manager
title: IccProfileRgb
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---


# IccProfileRgb{#iccprofilergb}

Perfil de cores de saída padrão RGB. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta RGB quando nenhum espaço de cor de saída for especificado com icc= e para determinados valores de cor RGB especificados com vários comandos de renderização de imagem, como bgc= e color=.

## Propriedades {#section-b4a1bd92e99047479a5036413525a6d9}

Sequência de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfil ICC deste catálogo de materiais ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil RGB.

## Padrão {#section-5809772f8e96438ab7626d323c66a4ba}

Herdado de `default::IccProfileRgb` se não estiver definido ou se estiver vazio.

## Consulte também {#section-732c17dece3a4575855c9b79a08d0067}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileSrcRgb](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcrgb.md#reference-2fb0f7cfc6e74813b82cd98ae165bd49),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
