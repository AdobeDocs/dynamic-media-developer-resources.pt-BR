---
description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos. As macros são definidas em arquivos de definição de macro separados, que podem ser anexados a catálogos de imagens ou ao catálogo padrão.
solution: Experience Manager
title: Macros de comando
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 0%

---


# Macros de comando{#command-macros}

As macros de comando fornecem atalhos nomeados para conjuntos de comandos. As macros são definidas em arquivos de definição de macro separados, que podem ser anexados a catálogos de imagens ou ao catálogo padrão.

`$ *`name`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> name</span></span> </p> </td> 
  <td class="stentry"> <p>Nome da macro. </p></td> 
 </tr> 
</table>

`*``*` O nome não diferencia maiúsculas de minúsculas e pode consistir em qualquer combinação de letras ASCII, números, &#39;-&#39;, &#39;_&#39; e &#39;.&#39; caracteres.

As macros podem ser chamadas em qualquer lugar em uma solicitação após o &#39;?&#39;, bem como em qualquer lugar dentro de um campo `catalog::Modifier` ou `catalog::PostModifier`. As macros só podem representar um ou mais comandos completos do Image Serving e devem ser separadas de outros comandos com separadores &#39;&amp;&#39;.

As invocações de macro são substituídas por suas sequências de substituição precocemente durante a análise. Comandos em macros substituirão os mesmos comandos na solicitação se ocorrerem antes da chamada de macro na solicitação. Isso é diferente de `catalog::Modifier`, onde os comandos na cadeia de caracteres de solicitação sempre substituirão os comandos na cadeia de caracteres `catalog::Modifier`, independentemente da posição na solicitação.

As macros de comando não podem ter valores de argumento, mas variáveis personalizadas podem ser usadas para transmitir valores da solicitação para a macro.

As macros podem ser aninhadas, com a seguinte restrição: Uma macro só pode ser invocada se já estiver definida no momento em que a definição da macro for analisada, seja pela exibição anterior no mesmo arquivo de definição de macro, ou colocando a definição de tal macro incorporada no arquivo de definição de macro padrão.

## Exemplo {#section-2f73d36ac8d64254a03bae5afeae2fb9}

As macros podem ser úteis se os mesmos atributos forem aplicados a imagens diferentes.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Podemos definir uma macro para os atributos comuns:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

A macro seria usada da seguinte maneira:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Como `wid=` é diferente para a terceira solicitação, simplesmente substituímos o valor *depois de* a macro é chamada (especificar `wid=`*antes* `$view$` não teria efeito).

## Consulte também {#section-8cdba0ed2480444ca61e719e54f8871c}

[catálogo::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) ,  [catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), Referência de definição de  [macro](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
