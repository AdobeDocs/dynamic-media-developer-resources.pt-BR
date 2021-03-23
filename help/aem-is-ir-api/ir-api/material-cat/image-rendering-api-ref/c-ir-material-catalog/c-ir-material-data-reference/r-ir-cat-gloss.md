---
description: Brilho da superfície Especifica o brilho relativo da superfície do material.
seo-description: Brilho da superfície Especifica o brilho relativo da superfície do material.
seo-title: Brilho
solution: Experience Manager
title: Brilho
uuid: 7db83f99-15ab-4c43-adfb-07ad0b0c9707
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# Brilho{#gloss}

Brilho da superfície Especifica o brilho relativo da superfície do material.

Esse valor é usado pelo renderizador para os seguintes fins:

* Selecione o mapa de iluminação quando `catalog::Illum` for -1.
* Controla a renderização do efeito de brilho (reflexão especular) em conjunto com `catalog::Type`.
* Controla os efeitos de renderização da reflexão 3D juntamente com `catalog::Type` e `catalog::Roughness`.

## Propriedades {#section-ddc475c0556f4f67b4cf62bd1bcd4bf7}

Número inteiro. Número percentual no intervalo 0...100. Opcional para todos os materiais. Usado apenas para vinhetas com vários mapas de reflexão ou vinhetas com recurso de reflexão 3D. Deixe em branco ou defina como -1 se não for conhecido ou se não for necessário.

## Padrão {#section-2352721073524f1a8d461f64a363aac9}

Um valor padrão é fornecido pela vinheta se esse valor estiver definido como -1.

## Consulte também {#section-0213bbdb7d6d4974a7c53822957717c1}

[brilho=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ,  [catálogo::Rigidez](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99),  [catálogo::Tipo](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161)
