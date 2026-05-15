---
title: Tipos de dados comuns
description: Os atributos e campos do catálogo podem conter dados de um dos seguintes tipos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9af44474-0512-452a-af9e-48918e9da6ca
TQID: 'https://experienceleague.adobe.com/bf3PkSBKhuIzaRglWXs6UH0RoikSPcRUZBIAFdOaHV0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 162
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
