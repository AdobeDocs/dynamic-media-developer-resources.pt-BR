---
description: Carimbo de data/hora de modificação da imagem padrão. Fornece um valor padrão para o TimeStamp do catálogo.
solution: Experience Manager
title: Carimbo de data/hora
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '186'
ht-degree: 0%

---

# Carimbo de data/hora{#timestamp}

Carimbo de data/hora de modificação da imagem padrão. Fornece um valor padrão para catalog::TimeStamp.

Se não for especificado, o servidor usará a data/hora de modificação deste [!DNL *`catalog`*.ini] arquivo.

## Propriedades {#section-647066e62ce44a84b627fdd0b2f7cfec}

Valor de data/hora. Pode ser o número inteiro de milissegundos desde a meia-noite, 1º de janeiro de 1970 UTC/GMT ou um valor de string de data/hora com um dos seguintes formatos:

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* está no intervalo de 0 a 23.

*`zzz`* é um código de fuso horário com 3 ou 4 caracteres, como `GMT` ou `PST`. O horário de verão deve ser contabilizado no código do fuso horário (por exemplo, `PST` para a Hora Padrão da Costa Oeste, vs `PDT` para Horário de verão do Pacífico).

*`offset`* é um deslocamento de fuso horário em horas ou horas:minutos, em relação a GMT. Por exemplo, `PDT` equivale a `GMT -7`.

Todos os elementos de valores de data/hora formatados com string devem estar presentes. Se o valor de data/hora não estiver formatado corretamente, ele será ignorado e a hora de modificação do [!DNL *`catalog`*.ini] arquivo é usado em seu lugar.

## Padrão {#section-ac465313c97943ed97d41ea852329177}

Se estiver vazio ou não estiver definido, o servidor usará o tempo de modificação de arquivo deste `*`catálogo`*.ini` arquivo.

## Consulte também {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catálogo::Carimbo de data/hora](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [attribute::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
