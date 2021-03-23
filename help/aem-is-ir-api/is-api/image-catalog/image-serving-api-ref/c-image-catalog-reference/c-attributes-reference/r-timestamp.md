---
description: Carimbo de data e hora padrão da modificação da imagem. Fornece um valor padrão para o catálogo TimeStamp.
seo-description: Carimbo de data e hora padrão da modificação da imagem. Fornece um valor padrão para o catálogo TimeStamp.
seo-title: TimeStamp
solution: Experience Manager
title: TimeStamp
uuid: 0670e53a-ad7d-46cf-8e18-4c52a766df6f
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# TimeStamp{#timestamp}

Carimbo de data e hora padrão da modificação da imagem. Fornece um valor padrão para catalog::TimeStamp.

Se não especificado, o servidor usará a data/hora de modificação deste arquivo [!DNL *`catalog`*.ini].

## Propriedades {#section-647066e62ce44a84b627fdd0b2f7cfec}

Valor de data/hora. Pode ser o número inteiro de milissegundos desde a meia-noite, 1º de janeiro de 1970 UTC/GMT ou um valor de string de data/hora com um dos seguintes formatos:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* está no intervalo de 0 a 23.

*`zzz`* é um código de fuso horário de 3 ou 4 caracteres, como  `GMT` ou  `PST`. O horário de verão deve ser contabilizado no código do fuso horário (por exemplo, `PST` para Horário Padrão do Pacífico vs `PDT` para Horário de Verão do Pacífico).

*`offset`* é um deslocamento de fuso horário em horas ou horas:minutos, em relação ao GMT. Por exemplo, `PDT` é equivalente a `GMT -7`.

Todos os elementos de valores de data/hora formatados na string devem estar presentes. Se o valor de data/hora não estiver formatado corretamente, ele será ignorado e a hora de modificação do arquivo [!DNL *`catalog`*.ini] será usada.

## Padrão {#section-ac465313c97943ed97d41ea852329177}

Se estiver vazio ou não estiver definido, o servidor usará a hora de modificação de arquivo desse arquivo `*`catalog`*.ini`.

## Consulte também {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catalog::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) ,  [atributo::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [atributo::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
