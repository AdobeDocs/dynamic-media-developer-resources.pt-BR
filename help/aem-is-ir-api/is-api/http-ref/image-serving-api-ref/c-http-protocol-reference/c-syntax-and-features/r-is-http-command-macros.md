---
title: Macros de comando
description: As macros de comando fornecem atalhos nomeados para conjuntos de comandos. As macros são definidas em arquivos de definição de macro separados, que podem ser anexados a catálogos de imagens ou ao catálogo padrão.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 304d93af-3427-4111-882a-35be9ec3aef5
TQID: 'https://experienceleague.adobe.com/a7vbT8heEkiWfmxn3wPudnzYTRN-H-I5D22038P4mJE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 311
ht-degree: 0%

---

# Macros de comando{#command-macros}

As macros de comando fornecem atalhos nomeados para conjuntos de comandos. As macros são definidas em arquivos de definição de macro separados, que podem ser anexados a catálogos de imagens ou ao catálogo padrão.

`$ *`nome`*$`

<table id="simpletable_A03541622C354F60B5F304B999C4EF8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nome</span></span> </p> </td> 
  <td class="stentry"> <p>Nome da macro. </p></td> 
 </tr> 
</table>

`*`name`*` não diferencia maiúsculas de minúsculas e pode consistir em qualquer combinação de letras ASCII, números , caracteres &#39;-&#39;, &#39;_&#39; e &#39;.&#39;.

As macros podem ser invocadas em qualquer lugar em uma solicitação depois do &#39;?&#39; e em qualquer lugar dentro de um campo `catalog::Modifier` ou `catalog::PostModifier`. As macros só podem representar um ou mais comandos completos do Servidor de imagens e devem ser separadas de outros comandos com separadores `&`.

As invocações de macro são substituídas por suas cadeias de caracteres de substituição no início da análise. Os comandos nas macros substituem os mesmos comandos na solicitação se ocorrerem antes da invocação da macro na solicitação. Esse fluxo de processamento é diferente de `catalog::Modifier`, onde os comandos na cadeia de caracteres da solicitação sempre substituem comandos na cadeia de caracteres `catalog::Modifier`, independentemente da posição na solicitação.

Macros de comandos não podem ter valores de argumento, mas variáveis personalizadas podem ser usadas para transmitir valores da solicitação para a macro.

As macros podem estar aninhadas. No entanto, uma macro só poderá ser invocada se já estiver definida no momento em que a definição da macro for analisada. Esse fluxo de trabalho é feito ao aparecer anteriormente no mesmo arquivo de definição de macro ou ao colocar a definição dessa macro incorporada no arquivo de definição de macro padrão.

## Exemplo {#section-2f73d36ac8d64254a03bae5afeae2fb9}

As macros podem ser úteis se os mesmos atributos forem aplicados a imagens diferentes.

`http://server/cat/1345?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/1435?wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1 http://server/cat/8243?wid=480&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

Você pode definir uma macro para os atributos comuns:

`view wid=240&fmt=jpeg&qlt=85&op_usm=5,2&bgc=200,200,200&align=-1,-1`

A macro seria usada da seguinte maneira:

`http://server/cat/1345?$view$ http://server/cat/1435?$view$ http://server/cat/8243?$view$&wid=480`

Como `wid=` é diferente para a terceira solicitação, você pode simplesmente substituir o valor *após* a macro é invocada (especificar `wid=`*antes* `$view$` não tem efeito).

## Consulte também {#section-8cdba0ed2480444ca61e719e54f8871c}

[catalog::MacroFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-macrofile.md#reference-f91d717b3847458ca0f1fe95387554a2) , [catalog::Modifier](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md), [Referência de Definição de Macro](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-macro-definition-reference/c-macro-definition-reference.md#concept-5ec73f7636c1496fba1e94094e694e79)
