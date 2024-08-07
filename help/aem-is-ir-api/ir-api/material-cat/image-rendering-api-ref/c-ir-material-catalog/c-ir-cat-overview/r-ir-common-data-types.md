---
title: Tipos de dados comuns
description: Os atributos e campos do catálogo podem conter dados de um dos seguintes tipos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# Tipos de dados comuns{#common-data-types}

Os atributos e campos do catálogo podem conter dados de um dos seguintes tipos.

**Cor**

Valor da cor. Valor de RGB hexadecimal compactado, opcionalmente precedido por 0x. Por exemplo, o valor de RGB `128,255,0` pode ser especificado como `0x80ff00` ou `80ff00`.

**Sinalizador**

`0`=false, `1`=true, qualquer outro valor significa desconhecido ou não especificado.

**Enumeração**

`0` indica um valor desconhecido ou não especificado, igual a um campo vazio. Os valores válidos de `enum` são números inteiros consecutivos, começando com 1.

**Número inteiro**

Valor inteiro assinado (por exemplo `0, -12, 34`). `0` ou valores negativos podem ter significado especial.

**Número real**

Valor de ponto flutuante assinado (por exemplo, `0, 12.5, 245 , -2.34e4`). 0 ou valores negativos podem ter significado especial.

**Cadeia de caracteres de texto**

Os delimitadores de cadeia são opcionais, a menos que a cadeia contenha `<CR>`, `<LF>` ou `<TAB>` caracteres. Aspas simples e duplas podem ser usadas como delimitadores. Se as aspas forem usadas, qualquer aspas inseridas na cadeia de caracteres deverá ser evitada usando duas aspas consecutivas (por exemplo, &#39; `This month''s Special`&#39;).
