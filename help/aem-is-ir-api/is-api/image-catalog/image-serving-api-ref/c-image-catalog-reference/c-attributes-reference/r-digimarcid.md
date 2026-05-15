---
description: Informações do usuário da Digimarc. Especifica as informações do usuário para incorporação de Digimarc.
solution: Experience Manager
title: DigimarcId
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac09c8cd-cb68-4b70-b1b4-9d4ca0166c7f
TQID: 'https://experienceleague.adobe.com/2kkvN1RLEhbDEmN4cA6lE5nGe9d-T3qcdxgGqF7L3Ig'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 134
ht-degree: 0%

---

# DigimarcId{#digimarcid}

Informações do usuário da Digimarc. Especifica as informações do usuário para incorporação de Digimarc.

## Propriedades {#section-1e11a36d9e0b4bf3858c4ab15fe7a272}

Cinco ou seis números inteiros separados por vírgulas. O terceiro e o quarto números não são mais usados:

`creator-id, creator-pin, durability [ , chroma ]`

O `creator-id` e o `creator-pin` são fornecidos pela Digimarc quando o serviço é comprado. Os valores não utilizados devem ser deixados em branco.

`durability` especifica a intensidade de incorporação da marca d&#39;água da Digimarc. Pode ser 1, 2, 3 ou 4, com 1 indicando a durabilidade mais fraca e 4 mais fortes.

Defina `chroma` como 1 para codificar a marca d&#39;água nos dados de crominância da imagem ou como 0 (padrão) para codificá-la na luminosidade. Essa configuração é ignorada ao gerar imagens em tons de cinza.

## Padrão {#section-d6ecb6e95a7b4232bd612834ea49e6bc}

Herdado de `default::DigimarcId` se não estiver definido ou se estiver vazio.

## Exemplo {#section-8469ae1c27b4461da3d53fbabc32d3c5}

Especifique uma ID de criador de Digimarc de teste com durabilidade definida como 4.

`DigimarcId= 404407,32,,,4`

## Consulte também {#section-75d4d2afd1df4127b31b1a82f30079d8}

[catalog::DigimarcInfo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-digimarcinfo-cat.md#reference-4925764ed683466bb7af4b807c86f8ba)
