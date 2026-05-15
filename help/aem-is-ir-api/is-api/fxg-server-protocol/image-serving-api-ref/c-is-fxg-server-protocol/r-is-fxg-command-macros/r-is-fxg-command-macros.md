---
title: Macros de comando
description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
TQID: 'https://experienceleague.adobe.com/DbXn35KC7OLFI0Dulgobj3UFPHnubmCisNDS541j8lE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 248
ht-degree: 0%

---

# Macros de comando{#command-macros}

As macros de comando fornecem atalhos nomeados para conjuntos de comandos.

As macros são definidas em arquivos de definição de macro separados, que podem ser anexados a catálogos de imagens ou ao catálogo padrão.

As macros podem ser invocadas em qualquer lugar em uma solicitação depois do &#39;?&#39; e em qualquer lugar dentro de um campo `catalog::Modifier`. As macros só podem representar um ou mais comandos completos do Servidor de imagens, portanto, elas devem ser delimitadas por separadores &quot;&amp;&quot; (exceto quando no início ou no fim da sequência do modificador).

As invocações de macro são substituídas por suas cadeias de caracteres de substituição no início da análise. Os comandos nas macros substituem os mesmos comandos na solicitação se ocorrerem antes da invocação da macro na solicitação. Esse fluxo é diferente de `catalog::Modifier`, em que os comandos na cadeia de caracteres da solicitação sempre substituem comandos na cadeia de caracteres `catalog::Modifier`, independentemente da posição na solicitação.

As macros podem ser aninhadas. No entanto, uma macro só poderá ser invocada se já estiver definida no momento em que a definição da macro for analisada. Esse fluxo é realizado ao aparecer anteriormente no mesmo arquivo de definição de macro ou ao colocar a definição dessa macro incorporada no arquivo de definição de macro padrão.

As macros podem ser úteis se os mesmos atributos forem aplicados a imagens diferentes.

[!DNL `http://server/cat/1345?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/1435?wid=240&fmt=pdf&imageRes=300`]

[!DNL `http://server/cat/8243?wid=480&fmt=pdf&imageRes=300`]

Você pode definir uma macro para os atributos comuns:

`view wid=240&fmt=pdf&imageRes=300`

A macro seria usada da seguinte maneira:

[!DNL `http://server/cat/1345?$view$`]

[!DNL `http://server/cat/1435?$view$`]

[!DNL `http://server/cat/8243?$view$&wid=480`]

Como `wid=` é diferente para a terceira solicitação, você simplesmente substitui o valor *após* a macro é invocada (especificando `wid=` *antes* `$view$`, que não tem efeito).

+ [name](r-name.md)
