---
description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos. As macros são definidas em arquivos separados de definição de macro, que podem ser anexados a catálogos de imagens ou ao catálogo padrão.
seo-description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos. As macros são definidas em arquivos separados de definição de macro, que podem ser anexados a catálogos de imagens ou ao catálogo padrão.
seo-title: Macros de comando
solution: Experience Manager
title: Macros de comando
topic: Scene7 Image Serving - Image Rendering API
uuid: a6ff5642-6716-484f-b37e-066994362a9b
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Macros de comando{#command-macros}

As macros de comando fornecem atalhos nomeados para conjuntos de comandos. As macros são definidas em arquivos separados de definição de macro, que podem ser anexados a catálogos de imagens ou ao catálogo padrão.

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>Nome da macro. </p></td> 
 </tr> 
</table>

` *`O `*` nome não diferencia maiúsculas de minúsculas e pode consistir em qualquer combinação de letras ASCII, números, &#39;-&#39;, &#39;_&#39; e &#39;.&#39; caracteres.

As macros podem ser chamadas em qualquer lugar em uma solicitação depois de &#39;?&#39;, bem como em qualquer lugar dentro de um campo `catalog::Modifier` ou `catalog::PostModifier`. As macros podem representar apenas um ou mais comandos completos do Serviço de Imagens e devem ser separadas de outros comandos com separadores &#39;&amp;&#39;.

As invocações de macro são substituídas por suas sequências de substituição precocemente durante a análise. Os comandos dentro de macros substituirão os mesmos comandos na solicitação se ocorrerem antes da chamada de macro na solicitação. Isso é diferente de `catalog::Modifier`, onde os comandos na string de solicitação sempre substituirão os comandos na string `catalog::Modifier`, independentemente da posição na solicitação.

As macros de comando não podem ter valores de argumento, mas variáveis personalizadas podem ser usadas para passar valores da solicitação para a macro.

As macros podem ser aninhadas, com a seguinte restrição: Uma macro só pode ser invocada se já estiver definida no momento em que a definição da macro for analisada, seja pela exibição anterior no mesmo arquivo de definição de macro ou colocando a definição para tal macro incorporada no arquivo de definição de macro padrão.

## Exemplo {#section-2f73d36ac8d64254a03bae5afeae2fb9}

As macros podem ser úteis se os mesmos atributos forem aplicados a imagens diferentes.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Podemos definir uma macro para os atributos comuns:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

A macro seria usada da seguinte forma:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Como `wid=` é diferente para a terceira solicitação, simplesmente substituímos o valor *depois de* a macro é chamada (especificar `wid=`*before* `$view$` não teria nenhum efeito).

## Consulte também {#section-8cdba0ed2480444ca61e719e54f8871c}

[catálogo::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ,  [catálogo::Modificador](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), Referência de definição de  [macro](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
