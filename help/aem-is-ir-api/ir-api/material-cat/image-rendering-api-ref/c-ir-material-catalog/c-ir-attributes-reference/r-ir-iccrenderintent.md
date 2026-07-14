---
title: IccRenderIntent
description: Tentativa de renderização de conversão de cor. Ela fornece a tentativa de renderização padrão para conversões de cores quando a intenção de renderização não é especificada com "icc=".
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 86cc907d-556c-40ec-a104-2f0dcf9ed1ce
TQID: 'https://experienceleague.adobe.com/5BehWh36v-kv7Z8kSj-WwoqBgyk4TC8srAhxKs89mnE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 101
ht-degree: 0%

---

# IccRenderIntent{#iccrenderintent}

Tentativa de renderização de conversão de cor. Fornece a tentativa de renderização padrão para conversões de cores quando a tentativa de renderização não é especificada com `icc=`.

## Propriedades {#section-0a38c60e1525426185616c42824aee2c}

Enum. Ajuste para 0 para perceptivo, 1 para colorimétrico relativo, 2 para saturação, 3 para colorimétrico absoluto. Mantenha vazio ou defina como qualquer outro valor para que você possa usar a tentativa de renderização padrão definida no perfil de cores.

## Padrão {#section-9301e3b7d0184ec5bf54a6eb73a6d3c1}

Herdado de `default::IccRenderIntent` se não estiver definido. Se vazio, a &quot;colorimétrica relativa&quot; é aplicada.

## Consulte também {#section-e77bcdfef6d2486ebd545631ccb40ebd}

[attribute::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127) , [attribute::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0), [`icc=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-icc.md#reference-86a2fff3cef24982ad2063d977a16e06)

