---
description: As variáveis de substituição são usadas para transferir valores do URL da solicitação para modelos de composição armazenados em catálogos de imagem. As variáveis também podem ser usadas para transmitir o mesmo valor a locais diferentes em uma solicitação complexa.
seo-description: As variáveis de substituição são usadas para transferir valores do URL da solicitação para modelos de composição armazenados em catálogos de imagem. As variáveis também podem ser usadas para transmitir o mesmo valor a locais diferentes em uma solicitação complexa.
seo-title: Variáveis de substituição
solution: Experience Manager
title: Variáveis de substituição
uuid: e369f2c3-8d89-4169-8869-f1d7ab89aab9
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---


# Variáveis de substituição{#substitution-variables}

As variáveis de substituição são usadas para transferir valores do URL da solicitação para modelos de composição armazenados em catálogos de imagem. As variáveis também podem ser usadas para transmitir o mesmo valor a locais diferentes em uma solicitação complexa.

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

Definições e referências de variáveis podem ocorrer na parte de consulta da solicitação, em `catalog::Modifier` e em `catalog::PostModifier`.

As variáveis são definidas como acima, semelhantes a outros comandos IS; o &#39;$&#39; à esquerda identifica o comando como uma definição de variável. As variáveis devem ser definidas antes de serem referenciadas.

O nome da variável *`var`* não diferencia maiúsculas de minúsculas e pode consistir em qualquer combinação de letras ASCII, números, &#39;-&#39;, &#39;_&#39; e &#39;.&#39;.

>[!NOTE]
>
>*`value`* deve ser codificado por URL de passagem única para transmissão HTTP segura. É necessária codificação dupla se *`value`* for retransmitido via HTTP. Esse é o caso quando *`value`* é substituído em uma solicitação externa aninhada ou no atributo href de um elemento SVG `<image>`.

As referências de variável consistem no nome da variável delimitado por &#39;$&#39; à esquerda e à direita ($*var*$). As referências podem ocorrer em qualquer parte da porção de valor de qualquer comando IS (ou seja, entre &#39;=&#39; após o nome do comando e o &#39;&amp;&#39; subsequente ou o final da solicitação). As variáveis personalizadas não podem ser aplicadas aos comandos `layer=` e `effect=`. Várias variáveis são permitidas no mesmo valor de comando. O servidor substitui cada ocorrência de ` $ *`var`*$` por *`value`*.

As referências de variáveis não podem ser aninhadas. Nenhuma ocorrência de ` $ *`var`*$` em *`value`* é substituída.

Por exemplo, o fragmento de solicitação:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

resolve:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; não é um caractere reservado; pode ocorrer de outra forma na solicitação. Por exemplo, `src=my$image$file.tif` é um comando válido (supondo que uma entrada de catálogo ou arquivo de imagem chamado `my$image$file.tif` existe), enquanto `wid=$number$` não é, porque `wid` requer um argumento numérico.

## Processamento de variável em solicitações aninhadas {#section-26d63adc446c4fa0808e11e8082abdfa}

` $ *`As variáveis `*$` podem ocorrer em qualquer lugar dentro das chaves de uma solicitação aninhada de Exibição de imagem ou Renderização de imagem, incluindo à esquerda do &#39;?&#39; separando o caminho da query. O servidor substitui essas referências por valores (do url ou de `catalog::Modifier` do catálogo de imagens principal) antes de analisar e processar a solicitação aninhada.

Além disso, todas as definições ` $ *`var`*=` do url ou `catalog::Modifier` são encaminhadas para todas as solicitações aninhadas de Exibição de imagem e Renderização de imagem. Isso garante que todas as definições de variável estejam disponíveis para todos os modelos, independentemente do nível de aninhamento.

Independentemente do nível de aninhamento, somente a codificação HTTP de passagem única deve ser aplicada a valores variáveis que devem ser substituídos em qualquer lugar nas solicitações aninhadas de Renderização de imagem ou Exibição de imagem ou nas strings `catalog::Modifier` associadas.

## Processamento de variável em solicitações externas incorporadas {#section-314e39a9aefb46faa737fd137897d1b0}

` $ *`As variáveis `*$` que ocorrem em qualquer lugar nas chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes. Isso permite que solicitações externas incorporadas sejam colocadas em um modelo em um catálogo de imagem.

Os valores de variáveis que devem ser substituídos em solicitações estrangeiras normalmente devem ser codificados duas vezes, já que nenhuma recodificação é aplicada antes que o servidor tente transmitir o url externo final.

## Processamento de variável em arquivos SVG {#section-a8359f9909764142b6a18ae778dca913}

` $ *`As variáveis `*$` podem ocorrer em arquivos SVG em valores de atributo e em  `<text>` sequências de caracteres. O Image Serving os substitui pelas definições ` $ *`var`*=` correspondentes conhecidas no nível de aninhamento da solicitação no qual o arquivo SVG é especificado.

>[!NOTE]
>
>Qualquer valor de variável que deva ser substituído em um valor de atributo `href` deve ser codificado em URL duplo; todos os outros devem ser codificados individualmente.

## Variável de caminho predefinida {#section-930d0dd12e8f49499becc9fe8df24092}

O *`object`* especificado no caminho da solicitação é atribuído à variável predefinida `*`$object`*`. &#39; ` $ *`object`*$`&#39; pode ser colocado em qualquer ponto da solicitação, no modelo referenciado pela solicitação ou em uma solicitação aninhada/incorporada, onde esse objeto é permitido, incluindo o valor `src=` e `mask=`, e o caminho de uma solicitação aninhada/incorporada.

Por exemplo, a solicitação a seguir reutilizará a imagem especificada no caminho como a fonte de uma camada em uma solicitação aninhada:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

É equivalente a

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

A definição de `*`$object`*` pode ser substituída pela especificação explícita de ` $ *`object`*=` com o valor desejado.

A variável de caminho predefinida geralmente é usada em conjunto com `template=`.

## Padrão {#section-b02483d15529444586a2e9504805b155}

Nenhum. Somente as variáveis que foram definidas serão substituídas pelo servidor (exceto a variável de caminho predefinida $object, que sempre será substituída). Qualquer ocorrência de ` $ *`var`*$` permanecerá literal se `*`var`*`não puder ser correspondida com uma definição de variável existente.

## Exemplos {#section-fba9393df6984247b7e30b3f93992e86}

Consulte &quot;Exemplo A&quot; em [Templates](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consulte também {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [template=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
