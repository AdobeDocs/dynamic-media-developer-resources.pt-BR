---
description: Resolução de miniatura padrão. Fornece um padrão para a resolução de objeto de miniatura caso um registro de catálogo específico não contenha um valor de ThumbRes de catálogo válido.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# ThumbRes{#thumbres}

Resolução de miniatura padrão. Fornece um padrão para a resolução de objeto de miniatura no caso de um registro de catálogo específico não conter um valor de catalog::ThumbRes válido.

Usado apenas para solicitações de miniatura ( `req=tmb`) e quando `catalog::ThumbType=3`.

## Propriedades {#section-88d37d0e030f4879a9e584dd2cc780f3}

Número real, maior que 0.Normalmente expresso como pixels por polegada, mas também pode estar em outras unidades, como pixels por metro.

## Padrão {#section-86588899ec9b4276a98b03d7faf64003}

Herdado de `default::ThumbRes` se não estiver definido ou se estiver vazio.

## Consulte também {#section-a6d2cce2e404441a996dba98a95c8e16}

[catálogo::ThumbRes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbres-cat.md#reference-eedb9991397347c3bed5bd0a785c4c69)
