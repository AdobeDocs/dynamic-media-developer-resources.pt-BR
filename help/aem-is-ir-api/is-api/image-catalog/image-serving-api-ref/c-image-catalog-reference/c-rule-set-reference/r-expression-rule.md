---
description: Elemento do padrão de expressão regular. Opcional em elementos <rule>.
solution: Experience Manager
title: expressão
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84b0bb22-7462-4038-9d14-2707999b5548
TQID: 'https://experienceleague.adobe.com/lYaMuefBswTJcGuSm7Rm-yNTpz1UbOkjJLpdCOdXNrQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 158
ht-degree: 0%

---

# expressão{#expression}

Elemento do padrão de expressão regular. Opcional em `<rule>` elementos.

## Atributos {#section-2d438c889ae84b6da7e0ed84b5d021a0}

Nenhum.

## Dados {#section-e2601008d71243109af1a8c55b58416d}

Sequência de caracteres de padrão de expressão regular.

## Descrição {#section-759bfb738ddb45dba1f0807aba8c1113}

O elemento `<expression>` pode estar vazio ou conter uma cadeia de caracteres de pesquisa simples ou um padrão de expressão regular. O padrão é aplicado a toda a string de solicitação.

Uma correspondência sempre ocorre quando `<expression>` está vazio ou não especificado; isso é equivalente a especificar `<expression>.*</expression>`.

A implementação é baseada no pacote Java [java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/), que fornece sintaxe de expressão regular semelhante à do Perl.

## Notas {#section-10b472a902674893b49ca49a7052c366}

A sequência de expressão não deve conter caracteres literais &lt; e &amp;. Esses caracteres reservados podem ser codificados com `&` e `<`, respectivamente, ou a cadeia inteira pode ser inserida em uma seção XML `CDATA`:

`<expression><![CDATA[&fmt=custom]]></expression>`

Todos os caracteres entre as marcas `<expression>` e `</expression>` são passados para o analisador de expressão regular, incluindo caracteres fora da seção `CDATA` opcional. Deve-se tomar cuidado para evitar espaços em branco extras.

## Consulte também {#section-ca98548917d945f4b71f18208f0e6840}

[java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
