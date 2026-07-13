---
title: Codificação HTTP de renderização de imagem
description: Os valores de comando devem ser codificados em http usando sequências de escape %xx, de modo que as cadeias de caracteres de valor não incluam os caracteres reservados '=', '&' e '%'.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a1efc4ce-a170-4bdb-8584-407e07113272
TQID: 'https://experienceleague.adobe.com/TNB9NbrGzMGS64CxHgj7aXlSHz8-KPBB0hMxB36mKvI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 0%

---

# Codificação HTTP de renderização de imagem{#image-rendering-http-encoding}

Os valores de comando devem ser codificados em http usando sequências de escape %xx, de modo que as cadeias de caracteres de valor não incluam os caracteres reservados &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39;.

Caso contrário, as regras de codificação HTTP padrão serão aplicadas. A especificação HTTP requer a codificação dos caracteres inseguros, como &#39; &#39; (espaço), &#39;&quot;&#39;(aspas duplas), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; e &#39;>&#39;, bem como quaisquer caracteres de controle, como `<return>` e `<tab>`.

**Cuidado:** As chaves { } usadas como delimitadores de aninhamento de solicitações não devem ser codificadas. Alguns clientes de email infelizmente codificam chaves na solicitação HTTP incorporada. Se esse problema ocorrer, a Renderização de imagem permitirá o uso de parênteses ( ) em vez de chaves.

## Exemplo {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

O fragmento de solicitação acima deve ser codificado da seguinte maneira:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Consulte também {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[Especificação HTTP/1.1 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)

