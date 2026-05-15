---
title: Macros de comando
description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 00f6d27e-9f6b-4eea-8f42-833fbc0f1c38
TQID: 'https://experienceleague.adobe.com/cXLJJQ5CS-Apmq-8qYV-ew-lcvfRjoNfIbl2qyyKB6U'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# Macros de comando{#command-macros}

As macros de comando fornecem atalhos nomeados para conjuntos de comandos.

`$ *[!DNL name]*$`

** *[!DNL name]* ** Nome da macro

As macros são definidas em arquivos de definição de macro separados, que podem ser anexados a catálogos de materiais ou ao catálogo padrão.

*[!DNL name]* não diferencia maiúsculas de minúsculas e pode consistir em qualquer combinação de letras ASCII, números , caracteres &#39;-&#39;, &#39;_&#39; e &#39;.&#39;.

Chame macros em qualquer lugar em uma solicitação depois do &#39;?&#39;, ou em qualquer lugar dentro de um campo `vignette::Modifier`. As macros só podem representar um ou mais comandos de Renderização de imagem e devem ser separadas de outros comandos com separadores &#39;&amp;&#39;.

As invocações de macro são substituídas por suas cadeias de caracteres de substituição no início da análise. Os comandos nas macros substituem os mesmos comandos na solicitação se ocorrerem antes da invocação da macro na solicitação. Este fluxo de trabalho é diferente de `vignette::Modifier`, no qual os comandos da cadeia de caracteres de solicitação substituem os comandos da cadeia de caracteres `vignette::Modifier`, independentemente da posição na solicitação.

Macros de comandos não podem ter valores de argumento, mas variáveis personalizadas podem ser usadas para transmitir valores da solicitação para a macro.

As macros não podem ser aninhadas.

**Exemplo**

As macros podem ser úteis se os mesmos comandos ou atributos forem aplicados a diferentes imagens renderizadas.

`http://server/ir/render/cat/vig0?fmt=jpeg&qlt=80&sharpen=1&src=cat/matA&res=40 http://server/ir/render/cat/vig1?fmt=jpeg&qlt=80&sharpen=1&src=cat/matB&res=40 http://server/ir/render/cat/vig2?fmt=jpeg&qlt=95&sharpen=1&src=cat/matC&res=40`

Você pode definir uma macro para os atributos comuns:

`render vignette=cat/$vig$&fmt=jpg&qlt=80&sharpen=1&src=cat/$mat$&res=40`

A macro seria usada da seguinte maneira:

`http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$ http://server/ir/render/cat/vig0?$mat=matc&$render$&qlt=95`

Como `qlt=` é diferente para a terceira solicitação, o software substitui o valor após a macro ser invocada (especificando `qlt=` *antes* `$render$`é ineficaz).

**Consulte também**

`catalog::MacroFile`, `catalog::Modifier`, Referência de Definição de Macro

<!--<a id="section_297B7FCB285F4891AA76DF8393089931"></a>-->
