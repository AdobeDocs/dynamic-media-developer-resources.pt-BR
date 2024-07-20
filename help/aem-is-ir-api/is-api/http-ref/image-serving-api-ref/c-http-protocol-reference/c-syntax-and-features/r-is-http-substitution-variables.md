---
description: As variáveis de substituição são usadas para transferir valores do URL da solicitação para modelos de composição armazenados em catálogos de imagem. As variáveis também podem ser usadas para transmitir o mesmo valor para locais diferentes em uma solicitação complexa.
solution: Experience Manager
title: Variáveis de substituição
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9fd73d16-e8bd-4fdb-a4e6-e86e5d219114
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '736'
ht-degree: 0%

---

# Variáveis de substituição{#substitution-variables}

As variáveis de substituição são usadas para transferir valores do URL da solicitação para modelos de composição armazenados em catálogos de imagem. As variáveis também podem ser usadas para transmitir o mesmo valor para locais diferentes em uma solicitação complexa.

` $ *`var`*= *`value`*`

<table id="simpletable_EFEC66C23CE949EFACDC415A954DF323"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome da variável. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> valor </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor com o qual a variável deve ser definida (string). </p> </td> 
 </tr> 
</table>

Definições e referências de variáveis podem ocorrer na parte de consulta da solicitação, em `catalog::Modifier`, e em `catalog::PostModifier`.

As variáveis são definidas como acima, de modo semelhante a outros comandos IS; o &#39;$&#39; à esquerda identifica o comando como uma definição de variável. As variáveis devem ser definidas antes de serem referenciadas.

O nome da variável *`var`* não diferencia maiúsculas de minúsculas e pode consistir em qualquer combinação de letras ASCII, números, &#39;-&#39;, &#39;_&#39; e &#39;.&#39;.

>[!NOTE]
>
>*`value`* deve ser codificado em URL de passagem única para transmissão HTTP segura. A codificação dupla será necessária se *`value`* for retransmitido por meio de HTTP. Este é o caso quando *`value`* é substituído em uma solicitação externa aninhada ou no atributo href de um elemento SVG `<image>`.

As referências de variável consistem no nome da variável delimitado por &#39;$&#39; à esquerda e à direita ($*var*$). As referências podem ocorrer em qualquer lugar na porção do valor de qualquer comando IS (isto é, entre o &#39;=&#39; após o nome do comando e o &#39;&amp;&#39; subsequente ou o fim da solicitação). Variáveis personalizadas não podem ser aplicadas aos comandos `layer=` e `effect=`. Várias variáveis são permitidas no mesmo valor de comando. O servidor substitui cada ocorrência de ` $ *`var`*$` por *`value`*.

As referências variáveis não podem ser aninhadas. Nenhuma ocorrência de ` $ *`var`*$` em *`value`* será substituída.

Por exemplo, o fragmento de solicitação:

`$var2=apple&$var1=my$var2$tree&text=$var1$`

resolve para:

`text=my$var2$tree`

>[!NOTE]
>
>&#39;$&#39; não é um caractere reservado; caso contrário, pode ocorrer na solicitação. Por exemplo, `src=my$image$file.tif` é um comando válido (supondo que exista uma entrada de catálogo ou arquivo de imagem chamado `my$image$file.tif`), enquanto `wid=$number$` não é, porque `wid` requer um argumento numérico.

## Processamento de variáveis em solicitações aninhadas {#section-26d63adc446c4fa0808e11e8082abdfa}

Referências de ` $ *`var`*$` podem ocorrer em qualquer lugar dentro das chaves de uma solicitação aninhada de Servidor de imagens ou de Renderização de imagens, inclusive à esquerda de &#39;?&#39; separar o caminho da consulta. O servidor substitui essas referências por valores (da url ou do `catalog::Modifier` do catálogo de imagens principal) antes de analisar e processar a solicitação aninhada.

Além disso, todas as definições ` $ *`var`*=` da url ou `catalog::Modifier` são encaminhadas para todas as solicitações aninhadas de Servidor de Imagens e de Renderização de Imagens. Isso garante que todas as definições de variável estejam disponíveis para todos os modelos, independentemente do nível de aninhamento.

Independentemente do nível de aninhamento, somente a codificação HTTP de passagem única deve ser aplicada a valores de variáveis que devem ser substituídos em qualquer lugar nas solicitações aninhadas de Renderização de imagem ou de Servidor de imagens ou suas `catalog::Modifier` cadeias de caracteres associadas.

## Processamento de variáveis em solicitações externas inseridas {#section-314e39a9aefb46faa737fd137897d1b0}

Referências ` $ *`var`*$` que ocorrem em qualquer lugar dentro das chaves de uma solicitação externa incorporada são substituídas por valores de definição de variável correspondentes. Isso permite que solicitações externas incorporadas sejam colocadas em um modelo em um catálogo de imagens.

Os valores de variáveis que devem ser substituídos em solicitações estrangeiras normalmente devem ser codificados duas vezes, já que nenhuma nova codificação é aplicada antes que o servidor tente transmitir o URL externo final.

## Processamento de variáveis em arquivos SVG {#section-a8359f9909764142b6a18ae778dca913}

Referências ` $ *`var`*$` podem ocorrer em arquivos SVG em valores de atributo e em `<text>` cadeias de caracteres. O Servidor de imagens os substitui pelas definições ` $ *`var`*=` correspondentes conhecidas no nível de aninhamento de solicitações em que o arquivo SVG é especificado.

>[!NOTE]
>
>Qualquer valor de variável que deve ser substituído em um valor de atributo `href` deve ser codificado por URL duplo; todos os outros devem ser codificados individualmente.

## Variável de caminho predefinida {#section-930d0dd12e8f49499becc9fe8df24092}

O *`object`* especificado no caminho da solicitação é atribuído à variável predefinida `*`$object`*`. O ` $ *`objeto`*$`&#39; pode ser colocado em qualquer lugar na solicitação, no modelo referenciado pela solicitação ou em uma solicitação aninhada/inserida onde esse objeto é permitido, incluindo o valor de `src=` e `mask=`, e o caminho de uma solicitação aninhada/inserida.

Por exemplo, a solicitação a seguir reutiliza a imagem especificada no caminho como a origem de uma camada em uma solicitação aninhada:

`/is/image/a/b?…&layer=3&src=is{…&src=$object$}&…`

É equivalente a

`/is/image/a/b?…&layer=3&src=is{…&src=a/b}&…`

A definição de `*`$object`*` pode ser substituída especificando explicitamente ` $ *`object`*=` com o valor desejado.

A variável de caminho predefinida é comumente usada em conjunto com `template=`.

## Padrão {#section-b02483d15529444586a2e9504805b155}

Nenhum. Somente as variáveis que foram definidas são substituídas pelo servidor (exceto a variável de caminho predefinida $object, que é sempre substituída). Qualquer ocorrência de ` $ *`var`*$` permanecerá literal se `*`var`*` não for compatível com uma definição de variável existente.

## Exemplos {#section-fba9393df6984247b7e30b3f93992e86}

Consulte o &quot;Exemplo A&quot; em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consulte também {#section-11b44cc824744f70b1705ebdd9ec4fe6}

[Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [modelo=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-template.md#reference-3beccaa462a64bf0ba867e5c8fd0bd14)
