---
title: IccProfileGray
description: Perfil de cor de saída padrão em tons de cinza. Especifica o nome do perfil de cores ICC a ser usado para imagens de resposta em tons de cinza quando nenhum espaço de cores de saída for especificado com icc= e para determinados valores de cores em tons de cinza especificados com vários comandos do Servidor de imagens, como color=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4964c3b3-799d-40cb-bc5f-d08acfd41ed9
TQID: 'https://experienceleague.adobe.com/brb4FvAJ9aMt3FylkuDbuRMEGabGuRqWBVD2Yu1y4os'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 148
ht-degree: 0%

---

# IccProfileGray{#iccprofilegray}

Perfil de cor de saída padrão em tons de cinza. Especifica o nome do perfil de cores ICC a ser usado para imagens de resposta em tons de cinza quando nenhum espaço de cores de saída for especificado com icc= e para determinados valores de cores em tons de cinza especificados com vários comandos do Servidor de imagens, como color=.

## Propriedades {#section-03f090ee2acf4537b83f78840d23ecab}

String de texto. Se especificado, deve ser um valor `icc::Name` válido do mapa de perfis ICC deste catálogo de imagens ou do catálogo padrão, ou um caminho de arquivo relativo a `attribute::RootPath`. O perfil ICC referenciado deve ser um perfil em tons de cinza.

## Padrão {#section-95ba3ab15edc4259b657c6ebf8783d61}

Herdado de `default::IccProfileGray` se não estiver definido ou se estiver vazio.

## Consulte também {#section-b737b9a6a8bd4997b660292301ba967b}

[icc::Name](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/r-name-icc.md#reference-9e7d3c8e35434981a3dfac66b8946cbe) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::IccProfileSrcGray](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilesrcgray.md#reference-a717831da24d43f680d01393660f12f9), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494)
