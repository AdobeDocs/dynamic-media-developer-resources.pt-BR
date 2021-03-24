---
description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos.
solution: Experience Manager
title: Macros de comando *
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---


# Macros de comando *{#command-macros}

As macros de comando fornecem atalhos nomeados para conjuntos de comandos.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Nome da macro

As macros são definidas em arquivos separados de definição de macro, que podem ser anexados a catálogos de materiais ou ao catálogo padrão.

*[!DNL name]* não diferencia maiúsculas de minúsculas e pode consistir de qualquer combinação de letras ASCII, números , &#39;-&#39;, &#39;_&#39; e &#39;.&#39; caracteres.

Chame macros em qualquer lugar em uma solicitação depois de &#39;?&#39; ou em qualquer lugar dentro de um campo `vignette::Modifier`. As macros só podem representar um ou mais comandos completos de Renderização de Imagem e devem ser separadas de outros comandos com separadores &#39;&amp;&#39;.

As invocações de macro são substituídas por suas sequências de substituição precocemente durante a análise. Os comandos em macros substituem os mesmos comandos na solicitação se ocorrerem antes da chamada de macro na solicitação. Isso é diferente de `vignette::Modifier`, onde os comandos na cadeia de caracteres de solicitação sempre substituirão os comandos na cadeia de caracteres `vignette::Modifier`, independentemente da posição na solicitação.

As macros de comando não podem ter valores de argumento, mas variáveis personalizadas podem ser usadas para transmitir valores da solicitação para a macro.

As macros podem não estar aninhadas.

**Exemplo**

As macros podem ser úteis se os mesmos comandos ou atributos forem aplicados a imagens renderizadas diferentes.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Você pode definir uma macro para os atributos comuns:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

A macro seria usada da seguinte maneira:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Como `qlt=` é diferente para a terceira solicitação, simplesmente substituímos o valor após a macro ser chamada (especificar `qlt=`*before* `$render$`não teria efeito).

**Consulte também**

`catalog::MacroFile`,  `catalog::Modifier`, Referência de definição de macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

