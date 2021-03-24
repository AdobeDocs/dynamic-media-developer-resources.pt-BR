---
description: Os valores de comando devem ser codificados em http usando %xx sequências de escape, de modo que as sequências de valor não incluam os caracteres reservados '=', '&' e '%'.
solution: Experience Manager
title: Codificação HTTP de renderização de imagem
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Codificação HTTP de renderização de imagem{#image-rendering-http-encoding}

Os valores de comando devem ser codificados em http usando %xx sequências de escape, de modo que as sequências de valor não incluam os caracteres reservados &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39;.

Caso contrário, as regras de codificação HTTP padrão se aplicam. A especificação HTTP requer a codificação dos caracteres não seguros, como &#39; (espaço), &#39;&quot;(aspas duplas), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; e &#39;>&#39;, bem como quaisquer caracteres de controle, como `<return>` e `<tab>`.

**Cuidado:** as chaves { } usadas como delimitadores de aninhamento de solicitação não devem ser codificadas. Certos clientes de email infelizmente codificam chaves em solicitações HTTP incorporadas. Caso isso seja um problema, a Renderização de imagem permite o uso de parênteses ( ) em vez de chaves.

## Exemplo {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

O fragmento de solicitação acima deve ser codificado da seguinte maneira:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Consulte também {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[Especificação HTTP/1.1 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
