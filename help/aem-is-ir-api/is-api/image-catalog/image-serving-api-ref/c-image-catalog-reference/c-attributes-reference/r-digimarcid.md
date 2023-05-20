---
description: Informações do usuário da Digimarc. Especifica as informações do usuário para incorporação de Digimarc.
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---

# DigimarcId{#digimarcid}

Informações do usuário da Digimarc. Especifica as informações do usuário para incorporação de Digimarc.

## Propriedades {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Cinco ou seis números inteiros separados por vírgulas. O terceiro e o quarto números não são mais usados:

`creator-id, creator-pin, durability [ , chroma ]`

A variável `creator-id` e `creator-pin` são fornecidos pela Digimarc quando o serviço é adquirido. Os valores não utilizados devem ser deixados em branco.

`durability` especifica a intensidade de incorporação da marca d&#39;água da Digimarc. Pode ser 1, 2, 3 ou 4, com 1 indicando a durabilidade mais fraca e 4 mais fortes.

Definir `chroma` para 1 para codificar a marca d&#39;água nos dados de crominância da imagem ou para 0 (padrão) para codificá-la na luminância. Essa configuração é ignorada ao gerar imagens em tons de cinza.

## Padrão {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Herdado de `default::DigimarcId` se não estiver definido ou se estiver vazio.

## Exemplo {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Especifique uma ID de criador de Digimarc de teste com durabilidade definida como 4.

`DigimarcId= 404407,32,,,4`

## Consulte também {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
