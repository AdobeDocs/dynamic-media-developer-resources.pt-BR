---
description: Perfil de cor de saída padrão CMYK. Especifica o nome do perfil de cores ICC a ser usado para imagens de resposta CMYK quando nenhum espaço de cores de saída for especificado com icc= e para determinados valores de cores CMYK especificados com vários comandos do Servidor de imagens, como color=.
solution: Experience Manager
title: IccProfileCmyk
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2bf83cf5-3fc9-42aa-a143-4b56e43ee4d1
TQID: 'https://experienceleague.adobe.com/G0UbfC77naL9ki0QEcpEYCX5Z4Tr3wt7YL2bQi8ZNEI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 148
ht-degree: 0%

---

# IccProfileCmyk{#iccprofilecmyk}

Perfil de cor de saída padrão CMYK. Especifica o nome do perfil de cores ICC a ser usado para imagens de resposta CMYK quando nenhum espaço de cores de saída for especificado com icc= e para determinados valores de cores CMYK especificados com vários comandos do Servidor de imagens, como color=.

## Propriedades {#section-d8b6102cc1c744d482f99808ccfcaa24}

String de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfis ICC deste catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil CMYK.

## Padrão {#section-62442df09a724950bfbdd0640b3e6678}

Herdado de `default::IccProfileCmyk` se não estiver definido ou se estiver vazio.

## Consulte também {#section-17071d1ed5ad469490fd715ba8f4d30d}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcCmyk](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrccmyk.md#reference-b57196dfe5db41fe88bd0828ed4ec728), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
