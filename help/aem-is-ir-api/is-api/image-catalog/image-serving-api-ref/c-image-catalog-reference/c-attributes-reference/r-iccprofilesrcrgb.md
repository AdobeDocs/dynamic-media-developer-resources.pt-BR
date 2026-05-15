---
description: Perfil de cor de entrada padrão do RGB. Especifica o nome do perfil de cores ICC a ser usado para imagens de origem do RGB que não incorporam um perfil de cores e para determinados valores de cores do RGB especificados com vários comandos do Servidor de imagens, como color=.
solution: Experience Manager
title: IccProfileSrcRgb
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfcbd9fe-e696-46e3-abbf-497dc55fe855
TQID: 'https://experienceleague.adobe.com/CPYMKHgIu7mllwz1C-EM190nZxHzJ3547TWIEevP1rc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 0%

---

# IccProfileSrcRgb{#iccprofilesrcrgb}

Perfil de cor de entrada padrão do RGB. Especifica o nome do perfil de cores ICC a ser usado para imagens de origem do RGB que não incorporam um perfil de cores e para determinados valores de cores do RGB especificados com vários comandos do Servidor de imagens, como color=.

## Propriedades {#section-3cd753196959462e9e674dab0b033d08}

String de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfis ICC deste catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil RGB.

## Padrão {#section-2c3cb2d9c9bf4aa7896e51b5d444ddee}

Herdado de `default::IccProfileSrcRgb` se não estiver definido ou se estiver vazio. Se `attribute::IccProfileSrcRgb` não for resolvido para um perfil válido, `attribute::IccProfileRgb` será usado.

## Consulte também {#section-d6e5c6eeaea4445ba7fb5737cd193a48}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileRgb](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilergb.md#reference-3479e7daac54404f84b06b98ca07b9df), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
