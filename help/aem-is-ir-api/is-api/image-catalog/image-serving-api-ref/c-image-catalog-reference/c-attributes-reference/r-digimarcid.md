---
description: Informações do usuário da Digimarc. Especifica as informações do usuário para incorporação Digimarc.
seo-description: Informações do usuário da Digimarc. Especifica as informações do usuário para incorporação Digimarc.
seo-title: DigimarcId
solution: Experience Manager
title: DigimarcId
topic: Scene7 Image Serving - Image Rendering API
uuid: 23f1952f-71b7-4b2a-917d-8161ea855ac9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# DigimarcId{#digimarcid}

Informações do usuário da Digimarc. Especifica as informações do usuário para incorporação Digimarc.

## Propriedades {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Cinco ou seis números inteiros separados por vírgulas. O terceiro e o quarto números não são mais usados:

`creator-id, creator-pin, durability [ , chroma ]`

Os `creator-id` e `creator-pin` são fornecidos pela Digimarc quando o serviço é adquirido. Os valores não utilizados devem ser deixados em branco.

`durability` especifica a intensidade de incorporação da marca d&#39;água Digimarc. Pode ser 1, 2, 3 ou 4, com 1 indicador de menor durabilidade e 4 maior.

Defina `chroma` como 1 para codificar a marca d&#39;água nos dados de crominância da imagem ou como 0 (padrão) para codificá-la na luminância. Essa configuração é ignorada ao produzir imagens em tons de cinza.

## Padrão {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Herdado de `default::DigimarcId` se não estiver definido ou se estiver vazio.

## Exemplo {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Especifique uma ID de criador da Digimarc de teste com durabilidade definida como 4.

`DigimarcId= 404407,32,,,4`

## Consulte também {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catálogo::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
