---
title: Carimbo de data/hora
description: Se `attribute::UseLastModified` estiver definido, o valor `catalog::TimeStamp` será retornado na resposta HTTP como um cabeçalho HTTP de última modificação.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5532b182-cc8c-4a51-844f-e70c758f80a1
TQID: 'https://experienceleague.adobe.com/Am7JECwqMWbky2JrHKqZV1BJ7ef06JP9Sy-g9uUo8tw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 0%

---

# Carimbo de data/hora{#timestamp}

Se `attribute::UseLastModified` estiver definido, o valor `catalog::TimeStamp` será retornado na resposta HTTP como um cabeçalho HTTP de Última Modificação. O cabeçalho Last-Modified sempre é retornado para conteúdo estático, mesmo se `attribute::UseLastModified` não estiver definido.

Para conteúdo de imagem e SVG, `catalog::TimeStamp` também é usado para validação de cache com base em catálogo (consulte [attribute::CacheValidationPolicy](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md).

## Propriedades {#section-2298a384b5cb43929542655c5a49beb2}

Valor de data/hora em formato Java. Pode ser o número inteiro de milissegundos desde a meia-noite, 1º de janeiro de 1970 UTC/GMT, ou um valor de string de data/hora com um dos seguintes formatos:

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* *`zzz`*

*`mm`*/ *`dd`*/ *`yyyy`* *`hh`*: *`mm`*: *`ss`* GMT *`offset`*

*`hh`* está no intervalo de 0 a 23.

*`zzz`* é um código de fuso horário com três ou quatro caracteres, como &quot;GMT&quot; ou &quot;PST&quot;. Conta para o Horário de verão no código do fuso horário. Por exemplo, &quot;PST&quot; para a Hora Padrão do Pacífico, versus &quot;PDT&quot; para o Horário de Verão do Pacífico).

*`offset`* é uma diferença de fuso horário em horas ou `hours:minutes`, relativa a GMT. Por exemplo, &#39;PDT&#39; equivale a &#39;GMT -7&#39;.

Todos os elementos de valores de data/hora formatados com string devem estar presentes. Se o valor de data/hora não estiver formatado corretamente, ele será ignorado e a hora de modificação do arquivo `*`catálogo`*.ini` será usada em seu lugar.

## Padrão {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` se o campo estiver vazio ou ausente.

## Consulte também {#section-c42a427aa4794c548408dc4de028d578}

[attribute::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296), [attribute::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8), [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
