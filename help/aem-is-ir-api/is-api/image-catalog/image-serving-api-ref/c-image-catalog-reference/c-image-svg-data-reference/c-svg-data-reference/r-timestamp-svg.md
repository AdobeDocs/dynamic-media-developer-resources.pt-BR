---
description: TimeStamp
solution: Experience Manager
title: TimeStamp
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9ce5e42e-573a-4e1c-97d4-98888e16ca56
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 0%

---


# Carimbo de data e hora{#timestamp}

Se `attribute::UseLastModified` estiver definido, o valor `catalog::TimeStamp` será retornado na resposta HTTP como um cabeçalho HTTP Última modificação. O cabeçalho Última modificação é sempre retornado para conteúdo estático, mesmo se `attribute::UseLastModified` não estiver definido.

Para imagens e conteúdo SVG, `catalog::TimeStamp` também é usado para validação de cache baseada em catálogo (consulte ` [attribute::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)`).

## Propriedades {#section-2298a384b5cb43929542655c5a49beb2}

Valor de data/hora no formato Java. Pode ser o número inteiro de milissegundos desde a meia-noite, 1º de janeiro de 1970 UTC/GMT, ou um valor de string de data/hora com um dos seguintes formatos:

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* *`zzz`*

*`mm`*/  *`dd`*/  *`yyyy`* *`hh`*:  *`mm`*:  *`ss`* GMT  *`offset`*

*`hh`* está no intervalo 0 - 23.

*`zzz`* é um código de fuso horário de três ou quatro caracteres, como &#39;GMT&#39; ou &#39;PST&#39;. Conta para Horário de verão no código de fuso horário. Por exemplo, &#39;PST&#39; para Horário Padrão do Pacífico, versus &#39;PDT&#39; para Horário de Verão do Pacífico).

*`offset`* é um deslocamento de fuso horário em horas ou  `hours:minutes`, em relação ao GMT. Por exemplo, &#39;PDT&#39; é equivalente a &#39;GMT -7&#39;.

Todos os elementos de valores de data/hora formatados da string devem estar presentes. Se o valor de data/hora não estiver formatado corretamente, ele será ignorado e a hora de modificação do arquivo `*`catálogo`*.ini` será usada.

## Padrão {#section-0cbf801401ff4857bdda168fd12358af}

`attribute::TimeStamp` se o campo estiver vazio ou não estiver presente.

## Consulte também {#section-c42a427aa4794c548408dc4de028d578}

[atributo::TimeStamp](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-timestamp.md#reference-4213c599a64942ee8cb9d80696b08296),  [atributo::UseLastModified](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-uselastmodified.md#reference-73ecc421e6864a38aec5a4775f06b8e8),  [atributo::CacheValidationPolicy](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-cachevalidationpolicy.md#reference-e55e52fd749041718a9af69fa2027b57)
