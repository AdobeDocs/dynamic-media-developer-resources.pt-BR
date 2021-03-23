---
description: Objetivo de renderização da conversão de cores. Fornece o propósito de renderização padrão para conversões de cores quando a intenção de renderização não é especificada com icc=.
seo-description: Objetivo de renderização da conversão de cores. Fornece o propósito de renderização padrão para conversões de cores quando a intenção de renderização não é especificada com icc=.
seo-title: IccRenderIntent
solution: Experience Manager
title: IccRenderIntent
uuid: a9648405-32c3-4762-bbb2-11e97d4f8374
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '126'
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
