---
description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos.
seo-description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos.
seo-title: Macros de comando
solution: Experience Manager
title: Macros de comando
uuid: f90d5132-aa5b-424f-a123-838723ed891a
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---


# Macros de comando{#command-macros}

As macros de comando fornecem atalhos nomeados para conjuntos de comandos.

As macros são definidas em arquivos de definição de macro separados, que podem ser anexados a catálogos de imagens ou ao catálogo padrão.

As macros podem ser chamadas em qualquer lugar em uma solicitação após o &#39;?&#39;, bem como em qualquer lugar dentro de um campo `catalog::Modifier`. As macros só podem representar um ou mais comandos completos do Image Serving, portanto, devem ser delimitadas por separadores &#39;&amp;&#39; (exceto quando no início ou no fim da string do modificador).

As invocações de macro são substituídas por suas sequências de substituição precocemente durante a análise. Comandos em macros substituirão os mesmos comandos na solicitação se ocorrerem antes da chamada de macro na solicitação. Isso é diferente de `catalog::Modifier`, onde os comandos na cadeia de caracteres de solicitação sempre substituirão os comandos na cadeia de caracteres `catalog::Modifier`, independentemente da posição na solicitação.

As macros podem ser aninhadas, com a seguinte restrição: uma macro só pode ser invocada se já estiver definida no momento em que a definição da macro for analisada, seja pela exibição anterior no mesmo arquivo de definição de macro, ou colocando a definição de tal macro incorporada no arquivo de definição de macro padrão.

As macros podem ser úteis se os mesmos atributos forem aplicados a imagens diferentes.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

Podemos definir uma macro para os atributos comuns:

`view wid=240&fmt=pdf&imageRes=300`

A macro seria usada da seguinte maneira:

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

Como `wid=` é diferente para a terceira solicitação, simplesmente substituímos o valor *depois de* a macro é chamada (especificar `wid=`*antes* `$view$` não teria efeito).

+ [name](r-name.md)
