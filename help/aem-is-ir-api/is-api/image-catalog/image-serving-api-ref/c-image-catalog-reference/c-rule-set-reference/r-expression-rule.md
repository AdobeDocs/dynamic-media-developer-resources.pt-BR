---
description: Elemento de padrão de expressão regular. Opcional em elementos <rule> .
seo-description: Elemento de padrão de expressão regular. Opcional em elementos <rule> .
seo-title: expressão
solution: Experience Manager
title: expressão
uuid: f2036015-a2c7-4392-86f6-4cdf3152839a
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---


# expressão{#expression}

Elemento de padrão de expressão regular. Opcional em elementos `<rule>`.

## Atributos {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Nenhum.

## Dados {#section-e2601008d71243109af1a8c55b58416d}

Sequência de caracteres do padrão de expressão regular.

## Descrição {#section-759bfb738ddb45dba1f0807aba8c1113}

O elemento `<expression>` pode estar vazio ou conter uma cadeia de caracteres de pesquisa simples ou um padrão de expressão regular. O padrão é aplicado a toda a cadeia de caracteres de solicitação.

Uma correspondência sempre ocorre quando `<expression>` está vazio ou não é especificado; isso equivale a especificar `<expression>.*</expression>`.

A implementação é baseada no pacote Java [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), que fornece sintaxe de expressão regular semelhante à de Perl.

## Notas {#section-10b472a902674893b49ca49a7052c366}

A sequência de expressão não deve conter caracteres literais &lt; e &amp;. Esses caracteres reservados podem ser codificados com `&` e `<`, respectivamente, ou a sequência inteira pode ser incluída em uma seção XML `CDATA`:

`<expression><![CDATA[&fmt=custom]]></expression>`

Todos os caracteres entre as tags `<expression>` e `</expression>` são passados para o analisador de expressão regular, incluindo caracteres fora da seção opcional `CDATA`. Deve-se ter cuidado para evitar espaços em branco adicionais.

## Consulte também {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
