---
description: O Image Serving suporta um mecanismo de pré-processamento de solicitação simples, que se baseia em regras de substituição e correspondência de expressões regulares.
seo-description: O Image Serving suporta um mecanismo de pré-processamento de solicitação simples, que se baseia em regras de substituição e correspondência de expressões regulares.
seo-title: Referência do conjunto de regras
solution: Experience Manager
title: Referência do conjunto de regras
uuid: 356e4939-c57d-459a-8e40-9b25e20fc0a3
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---


# Referência do conjunto de regras{#rule-set-reference}

O Image Serving suporta um mecanismo de pré-processamento de solicitação simples, que se baseia em regras de substituição e correspondência de expressões regulares.

Coleções de regras de pré-processamento (*rule sets*) podem ser anexadas a catálogos de imagens ou ao catálogo padrão. As regras no catálogo padrão se aplicam somente se a solicitação não identificar um catálogo de imagem principal específico.

As regras de pré-processamento de solicitação podem modificar o caminho e as partes de consulta de solicitações antes de serem processadas pelo analisador do Servidor de Plataforma, incluindo manipular o caminho, adicionar comandos, alterar valores de comando e aplicar modelos ou macros. As regras também podem ser usadas para configurar e substituir determinados recursos de segurança que normalmente são controlados apenas com atributos de catálogo, como ofuscação de solicitação, marcação de água, bem como limitar o serviço a endereços IP de cliente específicos.

Os conjuntos de regras são armazenados como arquivos de documento XML. O caminho relativo ou absoluto do arquivo do conjunto de regras deve ser especificado em `attribute::RuleSetFile`.

## Estrutura geral {#section-8bcbd91ea8a946f28051bde8ad21827f}

```
 <?xml version="1.0" encoding="UTF-8"?> 
<ruleset> 
   <rule> 
      <expression> 
<varname>
  expression 
</varname></expression> 
      <substitution> 
<varname>
  substitution 
</varname></substitution> 
      <addressfilter> 
<varname>
  addressFilter 
</varname></addressfilter> 
      <header> 
<varname>
  headerValue 
</varname></header>  
   </rule> 
</ruleset>
```

Os elementos `<?xml>` e `<ruleset>` são sempre necessários em um arquivo XML de conjunto de regras válido, mesmo se nenhuma regra real estiver definida.

Um elemento `<ruleset>` contendo qualquer número de elementos `<rule>` é permitido.

O conteúdo dos arquivos de regras de pré-processamento faz distinção entre maiúsculas e minúsculas.

## Validação do conjunto de regras {#section-d8d101a0b4d74580835e37d128d05567}

Uma cópia de [!DNL RuleSet.xsd] é fornecida na pasta de catálogo e deve ser usada para validar um arquivo de conjunto de regras antes de registrá-lo no arquivo [!DNL catalog.ini]. Observe que a Exibição de imagem usa uma cópia interna de [!DNL RuleSet.xsd] para validação.

## Pré-processamento de URL {#section-2c09a2d79ada46b994857c6a7fb4c13a}

Antes de qualquer outro processamento, uma solicitação HTTP de entrada é parcialmente analisada para determinar qual catálogo de imagem deve ser aplicado. Depois que o catálogo é identificado, o conjunto de regras para o catálogo selecionado (ou o catálogo padrão, se nenhum catálogo específico foi identificado) é aplicado.

Os elementos `<rule>` são pesquisados na ordem especificada para uma correspondência com o conteúdo do elemento `<expression>` ( *`expression`*).

Se um `<rule>` for correspondido, o *`substitution`* opcional será aplicado e a sequência de solicitação modificada será passada para o analisador de solicitação do servidor para processamento normal.

Se nenhuma correspondência bem-sucedida for feita quando o fim de `<ruleset>` for atingido, a solicitação será passada para o analisador sem modificação.

## O atributo OnMatch {#section-ed952fa55d99422db0ee68a2b9d395d3}

O comportamento padrão pode ser modificado com o atributo `OnMatch` do elemento `<rule>`. `OnMatch` pode ser definido como  `break` (padrão),  `continue`ou  `error`.

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Elemento e atributo</b> </th> 
   <th class="entry"> <b>Comportamento quando ocorre uma correspondência</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>O processamento da regra é encerrado imediatamente após a aplicação da substituição dessa regra. Padrão. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>A substituição é aplicada e o processamento continua com a próxima regra. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>O processamento da regra é encerrado imediatamente e um status de resposta de "solicitação recusada" é retornado ao cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Substituição de atributos de catálogo {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` os elementos podem, opcionalmente, definir atributos que substituem os atributos de catálogo correspondentes quando a regra for correspondida com êxito. Se várias regras correspondentes definirem o mesmo atributo, o último prevalecerá. Consulte a descrição do elemento ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)` para obter uma lista de atributos que podem ser controlados com regras.

## Expressões regulares {#section-3f77bb9a265147b38c645f63ab1bad8b}

A correspondência de strings simples funciona para aplicativos muito básicos, mas expressões regulares são necessárias na maioria das instâncias. Embora as expressões regulares sejam padrão do setor, a implementação específica varia de instância para instância.

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) descreve a implementação de expressão regular específica usada pelo Serviço de imagem.

## Substrações capturadas {#section-066e659406d5403599cd26ae35e80d68}

Para facilitar modificações complexas de URL, as subsequências de caracteres podem ser capturadas na expressão ao delimitar a subsequência de caracteres com parênteses (...). As subsequências capturadas são numeradas sequencialmente, começando por 1, de acordo com a posição dos parênteses à esquerda. As subsequências capturadas podem ser inseridas na substituição usando ` $ *`n`*`, onde *`n`* é o número de sequência da subsequência capturada.

## Gerenciar arquivos de conjunto de regras {#section-0598a608e4044bb4805fe93ceebe10a9}

Um arquivo de conjunto de regras pode ser anexado a cada catálogo de imagem com o atributo de catálogo `attribute::RuleSetFile`. Embora você possa editar o arquivo do conjunto de regras a qualquer momento, o servidor de imagem reconhece as alterações somente quando o catálogo de imagem associado é recarregado. Esse recarregamento ocorre quando o servidor da plataforma é iniciado ou reiniciado e sempre que o arquivo do catálogo principal, que tem um sufixo de arquivo [!DNL .ini], é modificado ou &quot;tocado&quot; para alterar a data do arquivo.

## Exemplos {#section-aa769437d967459299b83a4bf34fe924}

**Exemplo A.** Defina uma regra que aumente as configurações de qualidade da imagem se o nome da imagem tiver o sufixo &quot;  [!DNL _hg]&quot;:

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

A expressão de regra especifica uma correspondência que não diferencia maiúsculas e minúsculas de &quot; [!DNL _hg]&quot; no final da cadeia de caracteres do URL. O sufixo é substituído pela string de consulta especificada, que altera as configurações de qualidade da imagem. Observe que o caractere `?` na cadeia de caracteres de substituição é evitado, pois esse é um caractere especial em expressões regulares.

>[!NOTE]
>
>A codificação necessária para o caractere e comercial (&amp;). Como alternativa, a string de substituição pode ser fechada em um bloco CDATA:

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**Exemplo B.** Um aplicativo Web específico não permite sequências de consulta. Defina uma regra que traduza o elemento do caminho à direita `small`, `medium` ou `large` para um modelo, usando o restante do caminho como o nome da imagem. Por exemplo, `myCat/myImage/small` traduziria para `myCat/smallTemplate?src=myCat/myImage`.

Podemos usar subsequências para reestruturar a solicitação:

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## Consulte também {#section-9b748e7c5cff4759a70f96657bd43352}

[pacote java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
