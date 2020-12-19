---
description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos.
seo-description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos.
seo-title: Macros de comando
solution: Experience Manager
title: Macros de comando
topic: Scene7 Image Serving - Image Rendering API
uuid: f90d5132-aa5b-424f-a123-838723ed891a
translation-type: tm+mt
source-git-commit: 4169757880407b62addd0a70ef1807d8b195820b
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---


# Macros de comando{#command-macros}

As macros de comando fornecem atalhos nomeados para conjuntos de comandos.

As macros são definidas em arquivos separados de definição de macro, que podem ser anexados a catálogos de imagens ou ao catálogo padrão.

As macros podem ser chamadas em qualquer lugar em uma solicitação depois de &#39;?&#39;, bem como em qualquer lugar dentro de um campo `catalog::Modifier`. As macros podem representar apenas um ou mais comandos completos do Serviço de imagem, portanto, devem ser delimitadas por separadores &#39;&amp;&#39; (exceto quando no início ou no fim da string do modificador).

As invocações de macro são substituídas por suas sequências de substituição precocemente durante a análise. Os comandos dentro de macros substituirão os mesmos comandos na solicitação se ocorrerem antes da chamada de macro na solicitação. Isso é diferente de `catalog::Modifier`, onde os comandos na string de solicitação sempre substituirão os comandos na string `catalog::Modifier`, independentemente da posição na solicitação.

As macros podem ser aninhadas, com a seguinte restrição: uma macro só pode ser invocada se já estiver definida no momento em que a definição da macro for analisada, seja pela exibição anterior no mesmo arquivo de definição de macro ou colocando a definição para tal macro incorporada no arquivo de definição de macro padrão.

As macros podem ser úteis se os mesmos atributos forem aplicados a imagens diferentes.

[!DNL http://server/cat/1345?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/1435?wid=240&fmt=pdf&imageRes=300]

[!DNL http://server/cat/8243?wid=480&fmt=pdf&imageRes=300]

Podemos definir uma macro para os atributos comuns:

`view wid=240&fmt=pdf&imageRes=300`

A macro seria usada da seguinte forma:

[!DNL http://server/cat/1345?$view$]

[!DNL http://server/cat/1435?$view$]

[!DNL http://server/cat/8243?$view$&wid=480]

Como `wid=` é diferente para a terceira solicitação, simplesmente substituímos o valor *depois de* a macro é chamada (especificar `wid=`*before* `$view$` não teria nenhum efeito).

+ [name](r-name.md)
