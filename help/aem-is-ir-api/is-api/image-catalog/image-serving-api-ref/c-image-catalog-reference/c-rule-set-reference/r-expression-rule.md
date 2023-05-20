---
description: Elemento do padrão de expressão regular. Opcional em <rule> elementos.
solution: Experience Manager
title: expressão
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# expressão{#expression}

Elemento do padrão de expressão regular. Opcional em `<rule>` elementos.

## Atributos {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Nenhum.

## Dados {#section-e2601008d71243109af1a8c55b58416d}

Sequência de caracteres de padrão de expressão regular.

## Descrição {#section-759bfb738ddb45dba1f0807aba8c1113}

A variável `<expression>` O elemento pode estar vazio ou conter uma sequência de pesquisa simples ou um padrão de expressão regular. O padrão é aplicado a toda a string de solicitação.

Uma correspondência sempre ocorre quando `<expression>` está vazio ou não especificado; equivale a especificar `<expression>.*</expression>`.

A implementação é baseada no pacote Java [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), que fornece sintaxe de expressão regular semelhante à do Perl.

## Notas {#section-10b472a902674893b49ca49a7052c366}

A sequência de expressão não deve conter caracteres literais &lt; e &amp;. Esses caracteres reservados podem ser codificados com `&` e `<`, respectivamente, ou a cadeia de caracteres inteira pode ser inserida em um XML `CDATA` seção:

`<expression><![CDATA[&fmt=custom]]></expression>`

Todos os caracteres entre a variável `<expression>` e `</expression>` As tags são passadas para o analisador de expressão regular, incluindo caracteres fora do `CDATA` seção. Deve-se tomar cuidado para evitar espaços em branco extras.

## Consulte também {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
