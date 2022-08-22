---
title: Tipos de dados comuns
description: Os atributos e campos do catálogo podem conter dados de um dos seguintes tipos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# Tipos de dados comuns{#common-data-types}

Os atributos e campos do catálogo podem conter dados de um dos seguintes tipos.

**Cor**

Valor da cor. Valor hexadecimal de RGB compactado, precedido opcionalmente por 0x. Por exemplo, o valor RGB `128,255,0` pode ser especificado como `0x80ff00` ou `80ff00`.

**Sinalizador**

`0`=false, `1`=true, qualquer outro valor significa desconhecido ou não especificado.

**Enum**

`0` indica um valor desconhecido ou não especificado, o mesmo que um campo vazio. Válido `enum` são números inteiros consecutivos, começando com 1.

**Número inteiro**

Valor inteiro assinado (por exemplo, `0, -12, 34`). `0` ou valores negativos podem ter um significado especial.

**Número real**

Valor de ponto flutuante assinado (por exemplo, `0, 12.5, 245 , -2.34e4`). 0 ou valores negativos podem ter um significado especial.

**Sequência de texto**

Os delimitadores de string são opcionais, a menos que a string contenha qualquer `<CR>`, `<LF>`ou `<TAB>` caracteres. Aspas simples e duplas podem ser usadas como delimitadores. Se aspas forem usadas, qualquer aspas incorporadas à string deverá ser escapada usando duas aspas consecutivas (por exemplo, &#39; `This month''s Special`&quot;).
