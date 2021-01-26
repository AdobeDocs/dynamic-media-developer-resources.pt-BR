---
description: Propósito de renderização de conversão de cores. Fornece o propósito de renderização padrão para conversões de cores quando o propósito de renderização não é especificado com icc=.
seo-description: Propósito de renderização de conversão de cores. Fornece o propósito de renderização padrão para conversões de cores quando o propósito de renderização não é especificado com icc=.
seo-title: IccRenderIntent
solution: Experience Manager
title: IccRenderIntent
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a9648405-32c3-4762-bbb2-11e97d4f8374
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---


# IccRenderIntent{#iccrenderintent}

Propósito de renderização de conversão de cores. Fornece o propósito de renderização padrão para conversões de cores quando o propósito de renderização não é especificado com icc=.

## Propriedades {#section-0a38c60e1525426185616c42824aee2c}

Enum. Defina para 0 para a percepção, 1 para a colorimétrica relativa, 2 para a saturação, 3 para a colorimétrica absoluta. Mantenha vazio ou defina qualquer outro valor para usar o propósito de renderização padrão definido no perfil de cores.

## Padrão {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Herdado de `default::IccRenderIntent`se não estiver definido. Se estiver vazio, é aplicado &quot;colorimétrico relativo&quot;.

## Consulte também {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[atributo::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) ,  [atributo::IccBlackPointCompensação](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0),  [icc=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)
