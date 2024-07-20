---
description: Elemento de string de substituição. Opcional em elementos <rule>.
solution: Experience Manager
title: substituição
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# substituição{#substitution}

Elemento de string de substituição. Opcional em `<rule>` elementos.

## Atributos {#section-a4506fcb765f4f128f7f1f2629b18a6c}

Nenhum.

## Dados {#section-536b941e40a645cc8d3c6d63d6cbe0d7}

String de substituição.

## Descrição {#section-4a64a93f5e1a4d04a2db19166578bf76}

Define uma cadeia de caracteres de substituição para a cadeia de caracteres ou subcadeia correspondente no caminho ou na consulta.

Se a expressão padrão incluir subexpressões (delimitadas por parênteses), a primeira substring correspondente será substituída pela string de substituição. Se a expressão padrão não incluir subexpressões, toda a string correspondente será substituída.

Se `<expression>` estiver vazio ou ausente, a cadeia de caracteres de substituição será anexada ao caminho ou à consulta.

Se `<substitution>` estiver vazio, a cadeia ou subcadeia correspondente será removida. Se `<substitution>` não for especificado, o caminho ou a cadeia de consulta não será modificada.

>[!NOTE]
>
>Todas as correspondências na cadeia de caracteres de entrada são substituídas quando `replace="all"` é especificado no `<rule>`,element ao qual este elemento `<substitution>` pertence. Por padrão, somente a primeira correspondência é substituída pela cadeia de caracteres de substituição.

## Nota {#section-cedf2adabaaf441c9f598fb0ea180246}

A cadeia de caracteres de substituição não deve conter caracteres literais &lt; e &amp;. Esses caracteres reservados podem ser codificados com `&` e `<`, respectivamente, ou a cadeia de caracteres inteira pode ser inserida em uma seção CDATA XML:

`<substitution><![CDATA[&text=<Hello, world!>]]></ substitution>`
