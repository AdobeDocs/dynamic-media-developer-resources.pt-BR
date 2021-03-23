---
description: Os atributos e campos do catálogo podem conter dados de um dos seguintes tipos.
seo-description: Os atributos e campos do catálogo podem conter dados de um dos seguintes tipos.
seo-title: Tipos de dados comuns
solution: Experience Manager
title: Tipos de dados comuns
uuid: b36cf09d-dee2-4e8b-9500-e8fa4c5c112f
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---


# Tipos de dados comuns{#common-data-types}

Os atributos e campos do catálogo podem conter dados de um dos seguintes tipos.

**Cor**

Valor da cor. Valor RGB hexadecimal e compactado, precedido opcionalmente por 0x. Por exemplo, o valor RGB `128,255,0` pode ser especificado como `0x80ff00` ou `80ff00`.

**Sinalizador**

`0`=false,  `1`=true, qualquer outro valor significa desconhecido ou não especificado.

**Enum**

0 indica um valor desconhecido ou não especificado, o mesmo que um campo vazio. Valores válidos `enum` são números inteiros consecutivos, começando com 1.

**Número inteiro**

Valor inteiro assinado (por exemplo, 0, -12, 34). 0 ou valores negativos podem ter um significado especial.

**Número real**

Valor de ponto flutuante assinado (por exemplo, `0, 12.5, 245 , -2.34e4`). 0 ou valores negativos podem ter um significado especial.

**Sequência de texto**

Os delimitadores de string são opcionais, a menos que a string contenha qualquer caractere `<CR>`, `<LF>` ou `<TAB>`. Aspas simples e duplas podem ser usadas como delimitadores. Se aspas forem usadas, qualquer aspas incorporadas à string deverá ser evitada usando duas aspas consecutivas (por exemplo, &#39; `This month''s Special`&#39;).
