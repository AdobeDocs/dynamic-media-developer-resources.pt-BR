---
description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos.
seo-description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos.
seo-title: Macros de comando *
solution: Experience Manager
title: Macros de comando *
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0a131488-6296-4c7f-9bc7-3053df908899
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---


# Macros de comando *{#command-macros}

As macros de comando fornecem atalhos nomeados para conjuntos de comandos.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Nome da macro

As macros são definidas em arquivos separados de definição de macro, que podem ser anexados a catálogos de materiais ou ao catálogo padrão.

*[!DNL name]* não diferencia maiúsculas de minúsculas e pode consistir em qualquer combinação de letras ASCII, números, &#39;-&#39;, &#39;_&#39; e &#39;.&#39; caracteres.

Chame macros em qualquer lugar em uma solicitação depois de &#39;?&#39; ou em qualquer lugar dentro de um campo `vignette::Modifier`. As macros podem representar apenas um ou mais comandos completos de Renderização de imagem e devem ser separadas de outros comandos com separadores &#39;&amp;&#39;.

As invocações de macro são substituídas por suas sequências de substituição precocemente durante a análise. Os comandos dentro de macros substituem os mesmos comandos na solicitação se ocorrerem antes da chamada de macro na solicitação. Isso é diferente de `vignette::Modifier`, onde os comandos na string de solicitação sempre substituirão os comandos na string `vignette::Modifier`, independentemente da posição na solicitação.

As macros de comando não podem ter valores de argumento, mas variáveis personalizadas podem ser usadas para passar valores da solicitação para a macro.

As macros podem não estar aninhadas.

**Exemplo**

As macros podem ser úteis se os mesmos comandos ou atributos forem aplicados a imagens renderizadas diferentes.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

É possível definir uma macro para os atributos comuns:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

A macro seria usada da seguinte forma:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Como `qlt=` é diferente para a terceira solicitação, simplesmente substituímos o valor depois que a macro é chamada (especificar `qlt=`*before* `$render$`não teria nenhum efeito).

**Consulte também**

`catalog::MacroFile`,  `catalog::Modifier`, Referência de definição de macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->

