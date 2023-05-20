---
description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos.
solution: Experience Manager
title: Macros de comando
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dc149977-3ca8-4612-ad05-4d565440d00a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 0%

---

# Macros de comando{#command-macros}

As macros de comando fornecem atalhos nomeados para conjuntos de comandos.

As macros são definidas em arquivos de definição de macro separados, que podem ser anexados a catálogos de imagens ou ao catálogo padrão.

As macros podem ser invocadas em qualquer lugar em uma solicitação após &quot;?&quot;, bem como em qualquer lugar dentro de um `catalog::Modifier` campo. As macros só podem representar um ou mais comandos completos do Servidor de imagens, portanto, devem ser colocados por separadores &quot;&amp;&quot; (exceto quando no início ou no fim da sequência do modificador).

As invocações de macro são substituídas por suas cadeias de caracteres de substituição no início da análise. Os comandos nas macros substituirão os mesmos comandos na solicitação se ocorrerem antes da invocação da macro na solicitação. Isso é diferente de `catalog::Modifier`, em que os comandos na sequência de solicitação sempre substituirão os comandos na variável `catalog::Modifier` independentemente da posição na solicitação.

As macros podem ser aninhadas, com a seguinte restrição: uma macro só pode ser invocada se já estiver definida no momento em que a definição de macro for analisada, seja ao aparecer anteriormente no mesmo arquivo de definição de macro, ou ao colocar a definição de tal macro incorporada no arquivo de definição de macro padrão.

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

Desde `wid=` for diferente para a terceira solicitação, simplesmente substituímos o valor *após* a macro é invocada (especificando `wid=`*antes* `$view$` não teria qualquer efeito).

+ [name](r-name.md)
