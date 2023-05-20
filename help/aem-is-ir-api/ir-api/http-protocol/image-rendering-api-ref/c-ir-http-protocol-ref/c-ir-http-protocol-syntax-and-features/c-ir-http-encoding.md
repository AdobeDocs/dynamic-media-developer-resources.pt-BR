---
title: Codificação HTTP de renderização de imagem
description: Os valores de comando devem ser codificados em http usando sequências de escape %xx, de modo que as cadeias de caracteres de valor não incluam os caracteres reservados '=', '&' e '%'.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# Codificação HTTP de renderização de imagem{#image-rendering-http-encoding}

Os valores de comando devem ser codificados em http usando sequências de escape %xx, de modo que as cadeias de caracteres de valor não incluam os caracteres reservados &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39;.

Caso contrário, as regras de codificação HTTP padrão serão aplicadas. A especificação HTTP requer a codificação dos caracteres inseguros, como &#39; &#39; (espaço), &#39;&quot;&#39;(aspas duplas), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; e &#39;>&#39;, bem como quaisquer caracteres de controle, como `<return>` e `<tab>`.

**Atenção:** As chaves { } usadas como delimitadores de aninhamento de solicitações não devem ser codificadas. Alguns clientes de email infelizmente codificam chaves na solicitação HTTP incorporada. Se esse problema ocorrer, a Renderização de imagem permitirá o uso de parênteses ( ) em vez de chaves.

## Exemplo {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

O fragmento de solicitação acima deve ser codificado da seguinte maneira:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Consulte também {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[Especificação HTTP/1.1 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
