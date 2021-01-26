---
description: Elemento de string de substituição. Opcional em elementos <rule>.
seo-description: Elemento de string de substituição. Opcional em elementos <rule>.
seo-title: substituição
solution: Experience Manager
title: substituição
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f72902b1-0b0f-4401-9c3c-46573048cb25
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---


# substituição{#substitution}

Elemento de string de substituição. Opcional nos elementos `<rule>`.

## Atributos {#section-d955eefc53eb4274861270669c01f9ca}

Nenhum.

## Dados {#section-a2688866ed6d41279a8478886e511ae3}

Sequência de substituição.

## Descrição {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Define uma string de substituição para a string ou substring correspondente no caminho ou query.

Se a expressão de padrão incluir subexpressões (delimitadas com parênteses), a primeira substring correspondente será substituída pela string de substituição. Se a expressão de padrão não incluir subexpressões, toda a string correspondente será substituída.

Se `<expression>` estiver vazio ou ausente, a string de substituição será anexada ao caminho ou query.

Se `<substitution>` estiver vazio, a sequência de caracteres correspondente ou a subsequência de caracteres será removida. Se `<substitution>` não for especificado, o caminho ou a cadeia de caracteres do query não será modificada.

## Observação {#section-90fe89bb17a04804b7ff3c93df082892}

A cadeia de caracteres de substituição não deve conter caracteres literais &lt; e &amp;. Esses caracteres reservados podem ser codificados com `&` e `<`, respectivamente, ou a sequência inteira pode ser anexada em uma seção XML `CDATA`:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
