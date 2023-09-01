---
title: Macros de comando
description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos. As macros são definidas em arquivos de definição de macro separados, que podem ser anexados a catálogos de imagens ou ao catálogo padrão.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '310'
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

`*`name`*` não diferencia maiúsculas de minúsculas e pode consistir em qualquer combinação de letras ASCII, números , &#39;-&#39;, &#39;_&#39; e &#39;.&#39; caracteres.

As macros podem ser invocadas em qualquer lugar em uma solicitação após &quot;?&quot; e em qualquer lugar dentro de um `catalog::Modifier` ou `catalog::PostModifier` campo. As macros só podem representar um ou mais comandos completos do Servidor de imagens e devem ser separadas de outros comandos com `&` separadores.

As invocações de macro são substituídas por suas cadeias de caracteres de substituição no início da análise. Os comandos nas macros substituem os mesmos comandos na solicitação se ocorrerem antes da invocação da macro na solicitação. Esse fluxo de processamento é diferente de `catalog::Modifier`, em que os comandos na string de solicitação sempre substituem os comandos na variável `catalog::Modifier` independentemente da posição na solicitação.

Macros de comandos não podem ter valores de argumento, mas variáveis personalizadas podem ser usadas para transmitir valores da solicitação para a macro.

As macros podem estar aninhadas. No entanto, uma macro só poderá ser invocada se já estiver definida no momento em que a definição da macro for analisada. Esse fluxo de trabalho é feito ao aparecer anteriormente no mesmo arquivo de definição de macro ou ao colocar a definição dessa macro incorporada no arquivo de definição de macro padrão.

## Exemplo {#section-2f73d36ac8d64254a03bae5afeae2fb9}

As macros podem ser úteis se os mesmos atributos forem aplicados a imagens diferentes.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Você pode definir uma macro para os atributos comuns:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

A macro seria usada da seguinte maneira:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Porque `wid=` for diferente para a terceira solicitação, basta substituir o valor *após* a macro é invocada (especificando `wid=`*antes* `$view$` não tem efeito).

## Consulte também {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , [catálogo::Modificador](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), [Referência de definição de macro](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
