---
description: Espaço de cores padrão de escala de cinza. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta em tons de cinza quando nenhum espaço de cor de saída for especificado com icc=.
solution: Experience Manager
title: IccProfileGray
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 21f37090-a68c-4d86-a807-bda243a8f99e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---

# IccProfileGray{#iccprofilegray}

Espaço de cores padrão de escala de cinza. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta em tons de cinza quando nenhum espaço de cor de saída for especificado com icc=.

## Propriedades {#section-7af0a3e2c8cf4cdd98974bfa4a15f3ac}

Sequência de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfil ICC deste catálogo de materiais ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil em tons de cinza.

## Padrão {#section-aaa1c71e5d0c4e0792099d77e37c05ee}

Herdado de `default::IccProfileGray` se não estiver definido ou se estiver vazio.

## Consulte também {#section-cd43189611f4426aacddcc604eb02a10}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [attribute::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [attribute::IccProfileSrcGray](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrcgray.md#reference-a2abcd4aa5864738bbea8f55706deaf2),  [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
