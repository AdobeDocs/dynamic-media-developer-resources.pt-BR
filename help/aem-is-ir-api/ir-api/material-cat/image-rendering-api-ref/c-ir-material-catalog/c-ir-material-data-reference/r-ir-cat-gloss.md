---
description: Brilho da superfície Especifica o brilho relativo da superfície do material.
solution: Experience Manager
title: Brilho
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72c5d2f9-a7e6-4ad3-aebe-6a1b1fa5453f
TQID: 'https://experienceleague.adobe.com/Q1mOPjFXFnSPVRsvYpKs3a-15g1BfxQRCsFaMRBZNTw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 0%

---

# Brilho{#gloss}

Brilho da superfície Especifica o brilho relativo da superfície do material.

Esse valor é usado pelo renderizador para as seguintes finalidades:

* Selecione o mapa de iluminação quando `catalog::Illum` for -1.
* Controla a renderização do efeito de brilho (reflexão especular) em conjunto com `catalog::Type`.
* Controla efeitos de renderização de reflexão 3D em conjunto com `catalog::Type` e `catalog::Roughness`.

## Propriedades {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Número inteiro. Número percentual no intervalo de 0 a 100. Opcional para todos os materiais. Usado apenas para vinhetas com vários mapas de reflexão ou vinhetas com recurso de reflexão 3D. Deixe vazio ou defina -1 se não for conhecido ou não for necessário.

## Padrão {#section-2352721073524f1a8d461f64a363aac9}

Um valor padrão é fornecido pela vinheta se esse valor for definido como -1.

## Consulte também {#section-0213bbdb7d6d4974a7c53822957717c1}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) , [catálogo::Rugosidade](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99), [catálogo::Tipo](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)

