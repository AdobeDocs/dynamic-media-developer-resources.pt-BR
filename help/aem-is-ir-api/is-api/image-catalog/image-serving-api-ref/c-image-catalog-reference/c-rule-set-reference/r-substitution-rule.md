---
description: Elemento da cadeia de caracteres de substituição. Opcional em elementos <rule> .
seo-description: Elemento da cadeia de caracteres de substituição. Opcional em elementos <rule> .
seo-title: substituição
solution: Experience Manager
title: substituição
uuid: e5730559-0512-4416-927d-a7faf9180741
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---


# substituição{#substitution}

Elemento da cadeia de caracteres de substituição. Opcional em elementos `<rule>`.

## Atributos {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Nenhum.

## Dados {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

Sequência de caracteres de substituição.

## Descrição {#section-4a64a93f5e1a4d04a2db19166578bf76}

Define uma string de substituição para a string ou a substring correspondente no caminho ou na query.

Se a expressão de padrão incluir subexpressões (delimitadas por parênteses), a primeira substring correspondente será substituída pela string de substituição. Se a expressão de padrão não incluir subexpressões, toda a string correspondente será substituída.

Se `<expression>` estiver vazio ou ausente, a cadeia de caracteres de substituição será anexada ao caminho ou à consulta.

Se `<substitution>` estiver vazio, a cadeia de caracteres ou a subcadeia correspondente será removida. Se `<substitution>` não for especificado, o caminho ou a sequência de consulta não será modificada.

>[!NOTE]
>
>Todas as correspondências na cadeia de caracteres de entrada são substituídas quando `replace="all"` é especificado no elemento `<rule>`, ao qual este elemento `<substitution>` pertence. Por padrão, somente a primeira correspondência é substituída pela string de substituição.

## Observação {#section-cedf2adabaaf441c9f598fb0ea180246}

A sequência de substituição não deve conter caracteres literais &lt; e &amp;. Esses caracteres reservados podem ser codificados com `&` e `<`, respectivamente, ou a sequência inteira pode ser codificada em uma seção CDATA XML:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
