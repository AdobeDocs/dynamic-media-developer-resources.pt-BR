---
title: substituição
description: Elemento de string de substituição. Opcional em elementos <rule>.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea44d940-e8dd-4a25-a082-3ed3c0f57e45
TQID: 'https://experienceleague.adobe.com/GqJBLso7oigoeCJ-0KQzFv2aeoAiVzumjlDTtjBSDI4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 136
ht-degree: 0%

---

# substituição{#substitution}

Elemento de string de substituição. Opcional em `<rule>` elementos.

## Atributos {#section-d955eefc53eb4274861270669c01f9ca}

Nenhum.

## Dados {#section-a2688866ed6d41279a8478886e511ae3}

String de substituição.

## Descrição {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Define uma cadeia de caracteres de substituição para a cadeia de caracteres ou subcadeia correspondente no caminho ou na consulta.

Se a expressão padrão incluir subexpressões (delimitadas por parênteses), a primeira substring correspondente será substituída pela string de substituição. Se a expressão padrão não incluir subexpressões, toda a string correspondente será substituída.

Se `<expression>` estiver vazio ou ausente, a cadeia de caracteres de substituição será anexada ao caminho ou à consulta.

Se `<substitution>` estiver vazio, a cadeia ou subcadeia correspondente será removida. Se `<substitution>` não for especificado, o caminho ou a cadeia de consulta não será modificada.

## Nota {#section-90fe89bb17a04804b7ff3c93df082892}

A cadeia de caracteres de substituição não deve conter caracteres literais &lt; e &amp;. Esses caracteres reservados podem ser codificados com `&` e `<`, respectivamente, ou a cadeia inteira pode ser inserida em uma seção XML `CDATA`:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
