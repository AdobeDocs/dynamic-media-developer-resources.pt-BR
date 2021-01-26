---
description: Elemento de string de substituição. Opcional em elementos <rule>.
seo-description: Elemento de string de substituição. Opcional em elementos <rule>.
seo-title: substituição
solution: Experience Manager
title: substituição
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e5730559-0512-4416-927d-a7faf9180741
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# substituição{#substitution}

Elemento de string de substituição. Opcional nos elementos `<rule>`.

## Atributos {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Nenhum.

## Dados {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Sequência de substituição.

## Descrição {#section-4a64a93f5e1a4d04a2db19166578bf76}

Define uma string de substituição para a string ou substring correspondente no caminho ou query.

Se a expressão de padrão incluir subexpressões (delimitadas com parênteses), a primeira substring correspondente será substituída pela string de substituição. Se a expressão de padrão não incluir subexpressões, toda a string correspondente será substituída.

Se `<expression>` estiver vazio ou ausente, a string de substituição será anexada ao caminho ou query.

Se `<substitution>` estiver vazio, a sequência de caracteres ou a subsequência de caracteres correspondente será removida. Se `<substitution>` não for especificado, o caminho ou a cadeia de caracteres do query não será modificada.

>[!NOTE]
>
>Todas as correspondências na string de entrada são substituídas quando `replace="all"` é especificado no `<rule>` elemento ao qual este elemento `<substitution>` pertence. Por padrão, somente a primeira correspondência é substituída pela string de substituição.

## Observação {#section-cedf2adabaaf441c9f598fb0ea180246}

A cadeia de caracteres de substituição não deve conter caracteres literais &lt; e &amp;. Esses caracteres reservados podem ser codificados com `&` e `<`, respectivamente, ou a sequência inteira pode ser incluída em uma seção CDATA XML:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
