---
description: Espaço de cor padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta em escala cinza quando nenhum espaço de cor de saída for especificado com icc=.
seo-description: Espaço de cor padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta em escala cinza quando nenhum espaço de cor de saída for especificado com icc=.
seo-title: IccProfileCmyk
solution: Experience Manager
title: IccProfileCmyk
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d923d0fd-f00b-4fce-8ce9-8b177b4dba96
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# IccProfileCmyk{#iccprofilecmyk}

Espaço de cor padrão CMYK. Especifica o nome do perfil de cor ICC a ser usado para imagens de resposta em escala cinza quando nenhum espaço de cor de saída for especificado com icc=.

## Propriedades {#section-849678b272954bdcb236f49aa54f1609}

Sequência de caracteres de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfis ICC desse catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil CMYK.

## Padrão {#section-55026b7454af4d868bcb47f7743c9c5b}

Herdado de `default::IccProfileCmyk` se não estiver definido ou se estiver vazio.

## Consulte também {#section-89feb193693b43dc99a2107658d57154}

[icc::Name](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2) ,  [atributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40),  [atributo::IccProfileSrcCmyk](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilesrccmyk.md#reference-0256cae955404ebc92d5d0d1fa095ea2),  [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
