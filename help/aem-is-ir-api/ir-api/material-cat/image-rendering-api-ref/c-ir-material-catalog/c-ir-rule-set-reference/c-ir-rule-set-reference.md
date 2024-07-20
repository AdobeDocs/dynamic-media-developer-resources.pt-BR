---
description: A Renderização de imagem é compatível com um mecanismo de pré-processamento de solicitação simples que se baseia em regras de correspondência e substituição de expressão regular.
solution: Experience Manager
title: Referência do conjunto de regras
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 0%

---

# Referência do conjunto de regras{#rule-set-reference}

A Renderização de imagem é compatível com um mecanismo de pré-processamento de solicitação simples que se baseia em regras de correspondência e substituição de expressão regular.

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

Coleções de regras de pré-processamento (*conjuntos de regras*) podem ser anexadas a catálogos de materiais ou ao catálogo padrão. As regras no catálogo padrão se aplicam somente se a solicitação não anexar um catálogo de materiais específico.

As regras de pré-processamento de solicitações podem modificar o caminho e as partes de consulta de solicitações antes que elas sejam processadas pelo analisador de solicitações do servidor, incluindo manipulação do caminho, adição de comandos, alteração de valores de comando e aplicação de modelos ou macros. As regras também podem ser usadas para configurar e substituir alguns atributos de catálogo, bem como para limitar o serviço a endereços IP de clientes específicos.

Os conjuntos de regras são armazenados como arquivos de documento XML. O caminho relativo ou absoluto do arquivo de conjunto de regras deve ser especificado em `attribute::RuleSetFile`.

## Estrutura geral {#section-74faaee27fc543a2ab4a306f3a03674e}

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ruleset SYSTEM" RuleSet.dtd">
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
   </rule>
</ruleset>
```

Os elementos `<?xml>`, `<!DOCTYPE>` e `<ruleset>` são sempre necessários em um arquivo XML de conjunto de regras válido, mesmo se nenhuma regra real estiver definida.

Um elemento `<ruleset>` contendo qualquer número de elementos `<rule>` é permitido.

O conteúdo dos arquivos de regras de pré-processamento diferencia maiúsculas de minúsculas.

## Pré-processamento de URL {#section-737a38d1b8c746f995e64fa6cfbcec87}

Antes de qualquer outro processamento, uma solicitação HTTP de entrada é parcialmente analisada para determinar qual catálogo de materiais deve ser aplicado. Depois que o catálogo é identificado, o conjunto de regras do catálogo selecionado (ou o catálogo padrão, se nenhum catálogo específico foi identificado) é aplicado.

Os elementos `<rule>` são pesquisados na ordem especificada para uma correspondência com o conteúdo do elemento `<expression>` ( *`expression`*).

Se um `<rule>` for correspondido, o *`substitution`* opcional será aplicado e a cadeia de caracteres de solicitação modificada será passada para o analisador de solicitações do servidor para processamento normal.

Se nenhuma correspondência bem-sucedida for feita quando o final de `<ruleset>` for atingido, a solicitação será passada para o analisador sem modificação.

## O atributo OnMatch {#section-7a8ad3597780486985af5e9a3b1c7b56}

O comportamento padrão pode ser modificado com o atributo `OnMatch` dos elementos `<rule>`. `OnMatch` pode ser definido como `break` (padrão), `continue` ou `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Elemento e atributo </p> </th> 
   <th colname="col2" class="entry"> <p>Comportamento quando ocorre uma correspondência </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>O processamento de regras é encerrado imediatamente após a substituição dessa regra ter sido aplicada. Padrão. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>A substituição é aplicada e o processamento continua com a próxima regra. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;regra OnMatch="erro"&gt;</span> </p> </td> 
   <td colname="col2"> <p>O processamento de regras é encerrado imediatamente e um status de resposta "solicitação recusada" é retornado ao cliente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Substituição de atributos de catálogo {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` elementos podem, opcionalmente, definir atributos que substituem os atributos de catálogo correspondentes quando a regra é correspondida com êxito e `OnMatch="break"` é definido. Nenhum atributo é aplicado se `OnMatch="continue"` estiver definido. Consulte a descrição de `<rule>` para obter uma lista de atributos que podem ser controlados com regras.

## Expressões regulares {#section-4d326507b52544b0960a9a5f303e3fe6}

A correspondência de strings simples funciona para aplicativos muito básicos, mas expressões regulares são necessárias na maioria das instâncias. Embora as expressões regulares sejam padrão do setor, a implementação específica varia de instância para instância.

O [pacote java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) descreve a implementação da expressão regular específica usada pelo Servidor de imagens.

## Substrings capturadas {#section-8057cd65d48949ffb6a50e929bd3688b}

Para facilitar modificações complexas de URL, substrings podem ser capturadas na expressão ao colocar a substring entre parênteses (...). As subsequências de caracteres capturadas são numeradas sequencialmente, começando com 1 de acordo com a posição do parêntese inicial. As subsequências de caracteres capturadas podem ser inseridas na substituição usando *`$n`*, onde *`n`* é o número de sequência da subsequência de caracteres capturada.

## Gerenciamento de arquivos de conjunto de regras {#section-e8ce976b56404c009496426fd334d23d}

Um arquivo de conjunto de regras pode ser anexado a cada catálogo de materiais com o atributo de catálogo `attribute::RuleSetFile`. Embora você possa editar o arquivo de conjunto de regras a qualquer momento, o servidor de imagens reconhece as alterações somente quando o catálogo de materiais associado é recarregado. Isso acontece quando o [!DNL Platform Server] é iniciado ou reiniciado e sempre que o arquivo de catálogo principal (que tem um sufixo de arquivo [!DNL .ini]) é modificado ou &quot;tocado&quot; (para alterar a data do arquivo).

## Exemplos {#section-c4142a41f5cd4ff799a72fbc130c3700}

Os exemplos de conjunto de regras são fornecidos na seção correspondente da Referência ao catálogo de imagens na documentação do Servidor de imagens.

## Consulte também {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[pacote java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
