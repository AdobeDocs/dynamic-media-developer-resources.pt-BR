---
title: Carimbo de data/hora
description: Se `attribute::UseLastModified` estiver definido, o valor `catalog::TimeStamp` será retornado na resposta HTTP como um cabeçalho HTTP de última modificação. O cabeçalho Last-Modified sempre é retornado para conteúdo estático, mesmo se `attribute::UseLastModified` não estiver definido.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3c47b14d-b629-474d-952a-b09e1b1162b4
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '230'
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
