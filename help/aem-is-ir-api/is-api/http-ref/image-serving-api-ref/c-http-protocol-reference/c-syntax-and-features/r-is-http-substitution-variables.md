---
description: As variáveis de substituição são usadas para transferir valores do URL de solicitação para modelos de composição armazenados em catálogos de imagem. As variáveis também podem ser usadas para transmitir o mesmo valor para diferentes locais em uma solicitação complexa.
seo-description: As variáveis de substituição são usadas para transferir valores do URL de solicitação para modelos de composição armazenados em catálogos de imagem. As variáveis também podem ser usadas para transmitir o mesmo valor para diferentes locais em uma solicitação complexa.
seo-title: Variáveis de substituição
solution: Experience Manager
title: Variáveis de substituição
topic: Scene7 Image Serving - Image Rendering API
uuid: e369f2c3-8d89-4169-8869-f1d7ab89aab9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Variáveis de substituição{#substitution-variables}

As variáveis de substituição são usadas para transferir valores do URL de solicitação para modelos de composição armazenados em catálogos de imagem. As variáveis também podem ser usadas para transmitir o mesmo valor para diferentes locais em uma solicitação complexa.

` $ *``*= *`varvalue`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome da variável. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor ao qual a variável deve ser definida (string). </p> </td> 
 </tr> 
</table>

Definições e referências de variáveis podem ocorrer na parte do query da solicitação, em `catalog::Modifier` e em `catalog::PostModifier`.

As variáveis são definidas como acima, semelhantes a outros comandos IS; o &#39;$&#39; à esquerda identifica o comando como uma definição de variável. As variáveis devem ser definidas antes de serem referenciadas.

O nome da variável *`var`* não diferencia maiúsculas de minúsculas e pode consistir em qualquer combinação de letras ASCII, números, &#39;-&#39;, &#39;_&#39; e &#39;.&#39;.

>[!NOTE]
>
>*`value`* deve ser codificado em URL de passagem única para transmissão segura HTTP. A codificação do duplo é necessária se *`value`* for retransmitido via HTTP. Esse é o caso quando *`value`* é substituído em uma solicitação estrangeira aninhada ou no atributo href de um elemento SVG `<image>`.

As referências de variáveis consistem no nome da variável delimitado por &#39;$&#39; à esquerda e à direita ($*var*$). As referências podem ocorrer em qualquer parte do valor de qualquer comando IS (isto é, entre &#39;=&#39; após o nome do comando e o &#39;&amp;&#39; subsequente ou o fim da solicitação). As variáveis personalizadas não podem ser aplicadas aos comandos `layer=` e `effect=`. Várias variáveis são permitidas no mesmo valor de comando. O servidor substitui cada ocorrência de ` $ *`var`*$` por *`value`*.

As referências de variáveis não podem ser aninhadas. Nenhuma ocorrência de ` $ *`var`*$` em *`value`* é substituída.

Por exemplo, o fragmento de solicitação:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

resolve para:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; não é um caractere reservado; pode ocorrer de outra forma na solicitação. Por exemplo, `src=my$image$file.tif` é um comando válido (assumindo que existe uma entrada de catálogo ou um arquivo de imagem chamado `my$image$file.tif`), enquanto `wid=$number$` não é, porque `wid` requer um argumento numérico.

## Processamento de variável em solicitações aninhadas {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`As `*$` varreferências podem ocorrer em qualquer lugar dentro das chaves de uma solicitação aninhada de Serviço de imagem ou Renderização de imagem, incluindo à esquerda de &#39;?&#39; separando o caminho do query. O servidor substitui essas referências por valores (do url ou de `catalog::Modifier` do catálogo de imagens principal) antes de analisar e processar a solicitação aninhada.

Além disso, todas as definições ` $ *`var`*=` do url ou `catalog::Modifier` são encaminhadas para todas as solicitações aninhadas de Serviço de imagem e Renderização de imagem. Isso garante que todas as definições de variáveis estejam disponíveis para todos os modelos, independentemente do nível de aninhamento.

Independentemente do nível de aninhamento, somente a codificação HTTP de passagem única deve ser aplicada a valores variáveis que devem ser substituídos em qualquer lugar em solicitações aninhadas de Renderização de imagem ou de Serviço de imagem ou em suas strings `catalog::Modifier` associadas.

## Processamento de variável em solicitações externas incorporadas {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`as `*$` varreferências que ocorrem em qualquer lugar dentro das chaves de uma solicitação externa incorporada são substituídas pelos valores de definição de variável correspondentes. Isso permite que solicitações externas incorporadas sejam colocadas em um modelo em um catálogo de imagens.

Normalmente, os valores de variáveis que devem ser substituídos em solicitações estrangeiras devem ser codificados em duplo, já que nenhuma recodificação é aplicada antes que o servidor tente transmitir o url externo final.

## Processamento de variável em arquivos SVG {#section-a8359f9909764142b6a18ae778dca913}

` $ *`as `*$` varreferências podem ocorrer em arquivos SVG em valores de atributo e em  `<text>` strings. O Serviço de imagem os substitui pelas definições correspondentes ` $ *`var`*=` conhecidas no nível de aninhamento da solicitação no qual o arquivo SVG é especificado.

>[!NOTE]
>
>Qualquer valor de variável que deva ser substituído em um valor de atributo `href` deve ser codificado em URL de duplo; todos os outros devem ser codificados individualmente.

## Variável de caminho predefinida {#section-930d0dd12e8f49499becc9fe8df24092}

O *`object`* especificado no caminho da solicitação é atribuído à variável predefinida ` *`$object`*`. &#39; ` $ *`object`*$`&#39; pode ser colocado em qualquer local da solicitação, no modelo referenciado pela solicitação ou em uma solicitação aninhada/incorporada, na qual esse objeto é permitido, incluindo o valor de `src=` e `mask=`, e o caminho de uma solicitação aninhada/incorporada.

Por exemplo, a solicitação a seguir reutilizará a imagem especificada no caminho como a origem de uma camada em uma solicitação aninhada:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

Isso equivale a

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

A definição de ` *`$object`*` pode ser substituída especificando explicitamente ` $ *`object`*=` com o valor desejado.

A variável de caminho predefinida geralmente é usada em conjunto com `template=`.

## Padrão {#section-b02483d15529444586a2e9504805b155}

Nenhum. Somente as variáveis que foram definidas serão substituídas pelo servidor (exceto a variável de caminho predefinida $object, que sempre será substituída). Quaisquer ocorrências de ` $ *`var`*$` permanecerão literais se ` *`var`*`não puderem ser correspondidas com uma definição de variável existente.

## Exemplos {#section-fba9393df6984247b7e30b3f93992e86}

Consulte &quot;Exemplo A&quot; em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consulte também {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [modelo=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
