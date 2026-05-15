---
description: Elemento de string de substituição. Opcional em elementos <rule>.
solution: Experience Manager
title: substituição
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d0f1c558-b745-41dc-bf65-1bf1fdcb88d3
TQID: 'https://experienceleague.adobe.com/ZdC23CxEXKYN0d-h7nM8588KTS5Vy6BTh0kl5Iseq0w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 170
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
