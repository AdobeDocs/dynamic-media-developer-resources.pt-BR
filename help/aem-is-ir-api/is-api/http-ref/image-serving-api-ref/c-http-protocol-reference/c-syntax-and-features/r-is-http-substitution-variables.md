---
description: As variáveis de substituição são usadas para transferir valores do URL da solicitação para modelos de composição armazenados em catálogos de imagem. As variáveis também podem ser usadas para transmitir o mesmo valor a locais diferentes em uma solicitação complexa.
solution: Experience Manager
title: Variáveis de substituição
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Variáveis de substituição{#substitution-variables}

Substitution variables are used to transfer values from the request URL to compositing templates stored in image catalogs. Variables can also be used to convey the same value to different places in a complex request.

` $ *`var`*= *`value`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome da variável. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor ao qual a variável deve ser definida (string). </p> </td> 
 </tr> 
</table>

Variable definitions and references may occur in the query portion of the request, in `catalog::Modifier`, and in `catalog::PostModifier`.

As variáveis são definidas como acima, semelhantes a outros comandos IS; o &#39;$&#39; à esquerda identifica o comando como uma definição de variável. As variáveis devem ser definidas antes de serem referenciadas.

O nome da variável *`var`* não diferencia maiúsculas de minúsculas e pode consistir em qualquer combinação de letras ASCII, números, &#39;-&#39;, &#39;_&#39; e &#39;.&#39;.

>[!NOTE]
>
>*`value`* must be single-pass URL-encoded for safe HTTP transmission. A codificação dupla é necessária se *`value`* é retransmitido via HTTP. Isso ocorre quando *`value`* é substituído em uma solicitação externa aninhada ou no atributo href de um SVG `<image>` elemento.

As referências de variável consistem no nome da variável delimitado por &#39;$&#39; inicial e final ($*var*$). References may occur anywhere in the value portion of any IS commands (i.e. between the &#39;=&#39; following the command name and the subsequent &#39;&amp;&#39; or the end of the request). Custom variables cannot be applied to the `layer=` and `effect=` commands. Multiple variables are permitted in the same command value. The server substitutes each occurrence of ` $ *`var`*$` with *`value`*.

Variable references may not be nested. Any occurrences of ` $ *`var`*$` within *`value`* are not substituted.

For example, the request fragment:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

resolves to:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; is not a reserved character; it may occur otherwise in the request. Por exemplo, `src=my$image$file.tif` é um comando válido (supondo que uma entrada de catálogo ou arquivo de imagem chamado `my$image$file.tif` existe), while `wid=$number$` não, porque `wid` exige um argumento numérico.

## Processamento de variável em solicitações aninhadas {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`var`*$` references may occur anywhere within the curly braces of a nested Image Serving or Image Rendering request, including to the left of the &#39;?&#39; separando o caminho da query. O servidor substitui essas referências por valores (do url ou de `catalog::Modifier` do catálogo de imagens principal) antes de analisar e processar a solicitação aninhada.

Além disso, todos ` $ *`var`*=` definições do url ou `catalog::Modifier` são encaminhadas para todas as solicitações aninhadas de Exibição de imagem e Renderização de imagem. Isso garante que todas as definições de variável estejam disponíveis para todos os modelos, independentemente do nível de aninhamento.

Independentemente do nível de aninhamento, somente a codificação HTTP de passagem única deve ser aplicada a valores variáveis que devem ser substituídos em qualquer lugar nas solicitações aninhadas de Renderização de imagem ou Exibição de imagem ou em seus respectivos associados `catalog::Modifier` strings.

## Processamento de variável em solicitações externas incorporadas {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`var`*$` referências que ocorrem em qualquer lugar dentro das chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes. Isso permite que solicitações externas incorporadas sejam colocadas em um modelo em um catálogo de imagem.

Variable values which are to be substituted into foreign requests typically must be double-encoded, since no re-encoding is applied before the server attempts to transmit the final foreign url.

## Processamento de variável em arquivos SVG {#section-a8359f9909764142b6a18ae778dca913}

` $ *`var`*$` referências podem ocorrer em arquivos SVG em valores de atributo e em `<text>` strings. O Image Serving os substitui pelo correspondente ` $ *`var`*=` definições conhecidas no nível de aninhamento da solicitação em que o arquivo SVG é especificado.

>[!NOTE]
>
>Any variable value which is to be substituted into an `href` attribute value must be double URL-encoded; all others must be singly encoded.

## Variável de caminho predefinida {#section-930d0dd12e8f49499becc9fe8df24092}

O *`object`* especificado no caminho da solicitação é atribuído à variável predefinida `*`$object`*`. &#39; ` $ *`objeto`*$`&#39; pode ser colocado em qualquer local da solicitação, no modelo referenciado pela solicitação ou em uma solicitação aninhada/incorporada, onde esse objeto é permitido, incluindo o valor de `src=` e `mask=`e o caminho de uma solicitação aninhada/incorporada.

Por exemplo, a solicitação a seguir reutilizará a imagem especificada no caminho como a fonte de uma camada em uma solicitação aninhada:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

É equivalente a

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

A definição de `*`$object`*` pode ser substituído pela especificação explícita de ` $ *`objeto`*=` com o valor desejado.

A variável de caminho predefinida geralmente é usada juntamente com `template=`.

## Padrão {#section-b02483d15529444586a2e9504805b155}

Nenhum. Somente as variáveis que foram definidas são substituídas pelo servidor (exceto a variável de caminho predefinida $object, que sempre será substituída). Quaisquer ocorrências de ` $ *`var`*$` permanecer literal se `*`var`*`não pode corresponder a uma definição de variável existente.

## Examples {#section-fba9393df6984247b7e30b3f93992e86}

Consulte &quot;Exemplo A&quot; em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consulte também {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
