---
description: Elemento de padrão de expressão regular. Opcional em elementos <rule>.
solution: Experience Manager
title: expressão
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5fb95e93-cf14-4042-a338-d9d7df6e3b58
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# expressão{#expression}

Elemento de padrão de expressão regular. Opcional em `<rule>` elementos.

## Atributos {#section-fd0574eee1f9423cbb2ed709c0906800}

Nenhum.

## Dados {#section-4cd740c511a1432da0955e9acfbcf96f}

Sequência de caracteres de padrão de expressão regular.

## Descrição {#section-3245c8a531bb455d8398449f6ea63b37}

O elemento `<expression>` pode estar vazio ou conter uma cadeia de caracteres de pesquisa simples ou um padrão de expressão regular. O padrão é aplicado a toda a string de solicitação.

Uma correspondência sempre ocorre quando `<expression>` está vazio ou não especificado; isso é equivalente a especificar `<expression>.*</expression>`.

A implementação é baseada no pacote Java [java.util.regex](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-rule-set-reference/r-ir-expression.md#reference-49867deecb58412bbdc2ced564bbea3e), que fornece uma sintaxe de expressão regular semelhante à do Perl.

## Nota {#section-6b41a900b0ce4a9590e5861e3c81599c}

A sequência de expressão não deve conter caracteres literais &lt; e &amp;. Esses caracteres reservados podem ser codificados com `&` e `<`, respectivamente, ou a cadeia inteira pode ser inserida em uma seção XML `CDATA`:

`<expression><![CDATA[&fmt=custom]]></expression>`

Todos os caracteres entre as marcas `<expression>` e `</expression>` são passados para o analisador de expressão regular, incluindo caracteres fora da seção `CDATA` opcional. Deve-se tomar cuidado para evitar espaços em branco extras.

## Consulte também {#section-15a9fea18e644b8e9c498f5fd88e2eaa}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
