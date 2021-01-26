---
description: Os valores de comando devem ser codificados por http usando %xx sequências de escape, de modo que as strings de valor não incluam os caracteres reservados '=', '&' e '%'.
seo-description: Os valores de comando devem ser codificados por http usando %xx sequências de escape, de modo que as strings de valor não incluam os caracteres reservados '=', '&' e '%'.
seo-title: Codificação HTTP de renderização de imagem
solution: Experience Manager
title: Codificação HTTP de renderização de imagem
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 37bd0040-7bad-4548-ab39-7f598a217732
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---


# Codificação HTTP de renderização de imagem{#image-rendering-http-encoding}

Os valores de comando devem ser codificados por http usando %xx sequências de escape, de modo que as strings de valor não incluam os caracteres reservados &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39;.

Caso contrário, as regras de codificação HTTP padrão se aplicam. A especificação HTTP requer a codificação dos caracteres não seguros, como &#39; &#39; (espaço), &#39;&quot;&#39;(citação-duplo), &#39;#&#39;, &#39;%&#39;, &#39;&lt;&#39; e &#39;>&#39;, bem como quaisquer caracteres de controle, como `<return>` e `<tab>`.

**Cuidado: as chaves { }** usadas como delimitadores de aninhamento de solicitação não devem ser codificadas. Alguns clientes de email infelizmente codificam chaves na solicitação HTTP incorporada. Se isso for um problema, a renderização de imagem permite o uso de parênteses ( ) em vez de chaves.

## Exemplo {#section-3edc5b8ee2354220a281b01722ad337a}

`…&$text=rate&weight=85% 27#&…`

O fragmento de solicitação acima deve ser codificado da seguinte forma:

`…&$text=rate%26weight%3D85%25%2027%23&…`

## Consulte também {#section-d31268a02fe345e3abf0a4eb95a1dac5}

[Especificação HTTP/1.1 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
