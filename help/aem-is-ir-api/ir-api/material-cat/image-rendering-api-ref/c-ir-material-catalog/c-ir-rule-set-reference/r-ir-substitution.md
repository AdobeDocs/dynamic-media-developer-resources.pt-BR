---
description: Elemento da cadeia de caracteres de substituição. Opcional em elementos <rule> .
seo-description: Elemento da cadeia de caracteres de substituição. Opcional em elementos <rule> .
seo-title: substituição
solution: Experience Manager
title: substituição
uuid: f72902b1-0b0f-4401-9c3c-46573048cb25
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# substituição{#substitution}

Elemento da cadeia de caracteres de substituição. Opcional em elementos `<rule>`.

## Atributos {#section-d955eefc53eb4274861270669c01f9ca}

Nenhum.

## Dados {#section-a2688866ed6d41279a8478886e511ae3}

Sequência de caracteres de substituição.

## Descrição {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Define uma string de substituição para a string ou a substring correspondente no caminho ou na query.

Se a expressão de padrão incluir subexpressões (delimitadas por parênteses), a primeira substring correspondente será substituída pela string de substituição. Se a expressão de padrão não incluir subexpressões, toda a string correspondente será substituída.

Se `<expression>` estiver vazio ou ausente, a cadeia de caracteres de substituição será anexada ao caminho ou à consulta.

Se `<substitution>` estiver vazio, a sequência correspondente ou a substring será removida. Se `<substitution>` não for especificado, o caminho ou a sequência de consulta não será modificada.

## Observação {#section-90fe89bb17a04804b7ff3c93df082892}

A sequência de substituição não deve conter caracteres literais &lt; e &amp;. Esses caracteres reservados podem ser codificados com `&` e `<`, respectivamente, ou a sequência inteira pode ser incluída em uma seção XML `CDATA`:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
