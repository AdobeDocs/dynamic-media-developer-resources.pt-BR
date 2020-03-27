---
description: Elemento de string de substituição. Opcional em elementos <rule>.
seo-description: Elemento de string de substituição. Opcional em elementos <rule>.
seo-title: substituição
solution: Experience Manager
title: substituição
topic: Scene7 Image Serving - Image Rendering API
uuid: f72902b1-0b0f-4401-9c3c-46573048cb25
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# substituição{#substitution}

Elemento de string de substituição. Opcional em `<rule>` elementos.

## Atributos {#section-d955eefc53eb4274861270669c01f9ca}

Nenhum.

## Dados {#section-a2688866ed6d41279a8478886e511ae3}

Sequência de substituição.

## Descrição {#section-b6ab78ca5b0b4d508c71e553566cc9f3}

Define uma string de substituição para a string ou substring correspondente no caminho ou query.

Se a expressão de padrão incluir subexpressões (delimitadas com parênteses), a primeira substring correspondente será substituída pela string de substituição. Se a expressão de padrão não incluir subexpressões, toda a string correspondente será substituída.

Se `<expression>` estiver vazia ou ausente, a string de substituição será anexada ao caminho ou query.

Se `<substitution>` estiver vazio, a sequência correspondente ou a substring será removida. Se não `<substitution>` for especificado, o caminho ou a string de query não será modificada.

## Nota {#section-90fe89bb17a04804b7ff3c93df082892}

A cadeia de caracteres de substituição não deve conter caracteres literais &lt; e &amp;. Esses caracteres reservados podem ser codificados com `&` e `<`, respectivamente, ou a sequência inteira pode ser anexada em uma `CDATA` seção XML:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
