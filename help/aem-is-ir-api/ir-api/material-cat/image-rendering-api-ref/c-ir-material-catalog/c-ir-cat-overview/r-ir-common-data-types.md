---
description: Os atributos e campos do catálogo podem conter dados de um dos seguintes tipos.
seo-description: Os atributos e campos do catálogo podem conter dados de um dos seguintes tipos.
seo-title: Tipos de dados comuns
solution: Experience Manager
title: Tipos de dados comuns
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b36cf09d-dee2-4e8b-9500-e8fa4c5c112f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# Tipos de dados comuns{#common-data-types}

Os atributos e campos do catálogo podem conter dados de um dos seguintes tipos.

**Cor**

Valor da cor. Valor RGB hexadecimal, compactado, opcionalmente precedido por 0x. Por exemplo, o valor RGB `128,255,0` pode ser especificado como `0x80ff00` ou `80ff00`.

**Sinalizador**

`0`=false,  `1`=true, qualquer outro valor significa desconhecido ou não especificado.

**Enum**

0 indica um valor desconhecido ou não especificado, o mesmo que um campo vazio. Valores válidos de `enum` são números inteiros consecutivos, começando com 1.

**Número inteiro**

Valor inteiro assinado (por exemplo, 0, -12, 34). 0 ou valores negativos podem ter um significado especial.

**Número real**

Valor do ponto flutuante assinado (por exemplo, `0, 12.5, 245 , -2.34e4`). 0 ou valores negativos podem ter um significado especial.

**String de texto**

Os delimitadores de string são opcionais, a menos que a string contenha qualquer caractere `<CR>`, `<LF>` ou `<TAB>`. As aspas simples e duplos podem ser usadas como delimitadores. Se forem usadas aspas, qualquer aspas incorporadas dentro da string deve ser escapada usando duas aspas consecutivas (por exemplo, &#39; `This month''s Special`&#39;).
