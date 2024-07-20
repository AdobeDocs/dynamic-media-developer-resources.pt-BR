---
title: IccRenderIntent
description: Tentativa de renderização da conversão de cores. Ela fornece a tentativa de renderização padrão para conversões de cores quando "icc=" não é especificado para a tentativa de renderização.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 732b1935-6556-4420-a056-4e00cb3ed152
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# IccRenderIntent{#iccrenderintent}

Tentativa de renderização da conversão de cores. Fornece a tentativa de renderização padrão para conversões de cores quando a tentativa de renderização não é especificada com `icc=`.

## Propriedades {#section-2540099fb2fc47d29b04642da4f5922a}

Enum. Ajuste para 0 para perceptivo, 1 para colorimétrico relativo, 2 para saturação, 3 para colorimétrico absoluto.

## Padrão {#section-61a05067905b44099c228e15de279dbd}

Herdado de `default::IccRenderIntent` se não estiver definido ou se estiver vazio.

## Consulte também {#section-7da9ff3038ca452a9f7375a1ca0581af}

[attribute::IccProfile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) &#42;, [attribute::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [`icc=`](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-icc.md#reference-182b5679e21e4df3b4d330535a5a7517)
