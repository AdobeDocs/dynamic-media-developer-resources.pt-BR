---
title: Carimbo de data/hora
description: Carimbo de data/hora de modificação da imagem padrão. Ela fornece um valor padrão para o TimeStamp do catálogo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e137f795-e0f7-4b72-b7e8-188e254bbb45
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Carimbo de data/hora{#timestamp}

Carimbo de data/hora de modificação da imagem padrão. Fornece um valor padrão para catalog::TimeStamp.

Se não for especificado, o servidor usa a data/hora de modificação deste arquivo [!DNL *`catalog`*.ini].

## Propriedades {#section-647066e62ce44a84b627fdd0b2f7cfec}

Valor de data/hora. Pode ser o número inteiro de milissegundos desde meia-noite, 1º de janeiro de 1970 UTC/GMT, ou um valor de string de data/hora com um dos seguintes formatos:

O valor de data/hora *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss zzz`*

O valor de data/hora *`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

O valor de hora *`hh`* está no intervalo 0-23.

O valor de hora *`zzz`* é um código de fuso horário com três ou quatro caracteres, como `GMT` ou `PST`. O horário de verão deve ser contabilizado no código do fuso horário (por exemplo, `PST` para o Horário Padrão do Pacífico, vs `PDT` para o Horário de Verão do Pacífico).

O valor de hora *`offset`* é uma diferença de fuso horário em horas ou horas:minutes, relativa a GMT. Por exemplo, `PDT` é equivalente a `GMT -7`.

Todos os elementos de valores de data/hora formatados em sequência devem estar presentes. Se o valor de data/hora não estiver formatado corretamente, ele será ignorado e a hora de modificação do arquivo [!DNL *`catalog`*.ini] será usada em seu lugar.

## Padrão {#section-ac465313c97943ed97d41ea852329177}

Se estiver vazio ou não definido, o servidor usa a hora de modificação deste arquivo de `*`catálogo`*.ini`.

## Consulte também {#section-ea19bcefa4a04d7eb5d9480cf0e2ca26}

[catálogo::CarimboHora](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded) , [atributo::UseLastModified](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [atributo::CacheValidationPolicy](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
