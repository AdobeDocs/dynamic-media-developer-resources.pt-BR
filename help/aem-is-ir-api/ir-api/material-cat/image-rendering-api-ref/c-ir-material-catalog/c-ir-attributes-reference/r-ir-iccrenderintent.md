---
description: Objetivo de renderização da conversão de cores. Fornece o propósito de renderização padrão para conversões de cores quando a intenção de renderização não é especificada com icc=.
solution: Experience Manager
title: IccRenderIntent
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# IccRenderIntent{#iccrenderintent}

Objetivo de renderização da conversão de cores. Fornece o propósito de renderização padrão para conversões de cores quando a intenção de renderização não é especificada com icc=.

## Propriedades {#section-0a38c60e1525426185616c42824aee2c}

Enum. Defina como 0 para percepção, 1 para colorimétrica relativa, 2 para saturação, 3 para colorimétrica absoluta. Mantenha vazio ou definido como qualquer outro valor para usar o propósito de renderização padrão definido no perfil de cores.

## Padrão {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Herdado de `default::IccRenderIntent`se não estiver definido. Se estiver vazio, será aplicado &#39;relativa colorimetric&#39;.

## Consulte também {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[atributo: IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ,  [atributo::IccBlackPointCompensação](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0),  [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
