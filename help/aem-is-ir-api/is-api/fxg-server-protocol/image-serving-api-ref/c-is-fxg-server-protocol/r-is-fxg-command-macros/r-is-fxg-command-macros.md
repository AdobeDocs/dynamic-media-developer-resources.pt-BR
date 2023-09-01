---
title: Macros de comando
description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Macros de comando{#command-macros}

As macros de comando fornecem atalhos nomeados para conjuntos de comandos.

As macros são definidas em arquivos de definição de macro separados, que podem ser anexados a catálogos de imagens ou ao catálogo padrão.

As macros podem ser invocadas em qualquer lugar em uma solicitação após &quot;?&quot; e em qualquer lugar dentro de um `catalog::Modifier` campo. As macros só podem representar um ou mais comandos completos do Servidor de imagens, portanto, elas devem ser delimitadas por separadores &quot;&amp;&quot; (exceto quando no início ou no fim da sequência do modificador).

As invocações de macro são substituídas por suas cadeias de caracteres de substituição no início da análise. Os comandos nas macros substituem os mesmos comandos na solicitação se ocorrerem antes da invocação da macro na solicitação. Esse fluxo é diferente de `catalog::Modifier`, em que os comandos na string de solicitação sempre substituem os comandos na variável `catalog::Modifier` independentemente da posição na solicitação.

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

Porque `wid=` for diferente para a terceira solicitação, basta substituir o valor *após* a macro é invocada (especificando `wid=` *antes* `$view$` não tem efeito).

+ [name](r-name.md)
