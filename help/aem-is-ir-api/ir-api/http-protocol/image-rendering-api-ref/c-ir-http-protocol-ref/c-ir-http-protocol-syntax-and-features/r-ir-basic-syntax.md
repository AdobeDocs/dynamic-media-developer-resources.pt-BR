---
title: Sintaxe básica do protocolo HTTP de renderização de imagem
description: Esta seção descreve a sintaxe básica do protocolo HTTP de renderização de imagem do Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 0%

---

# Sintaxe básica do protocolo HTTP de renderização de imagem{#image-rendering-http-protocol-basic-syntax}

Esta seção descreve a sintaxe básica do protocolo HTTP de renderização de imagem do Dynamic Media.

<table id="table_0A7D7207EE6D4B08B62BE8620EBE0B25"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Item </p> </th> 
   <th colname="col2" class="entry"> <p>Definição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> solicitação</span> </p> </td> 
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vinheta</span> ] [ ?<span class="varname"> modificadores</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> server </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> porta</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vinheta </span> </p> </td> 
   <td colname="col2"> <p>Especificador de vinheta (caminho de arquivo relativo ou entrada de catálogo de vinheta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificadores </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modificador</span> *[ &amp; <span class="varname"> modificador</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificador </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> comando</span> | { $ <span class="varname"> macro</span> $ } | { .<span class="varname"> comentário</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> comando </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> value</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro </span> </p> </td> 
   <td colname="col2"> <p>Nome de uma macro de comando. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> comentário </span> </p> </td> 
   <td colname="col2"> <p>Sequência de comentários (ignorada pelo servidor). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName </span> </p> </td> 
   <td colname="col2"> <p>Nome de um comando ou atributo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var </span> </p> </td> 
   <td colname="col2"> <p>Nome de uma variável personalizada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> value </span> </p> </td> 
   <td colname="col2"> <p>Valor do comando ou da variável. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`*, e *`var`* não diferenciam maiúsculas de minúsculas. O servidor preserva as letras maiúsculas e minúsculas de todos os outros valores de string.

**Identificador do servidor**

O &#39; `/ir/render`O contexto raiz &#39;&#39; é necessário para todas as solicitações HTTP para a Renderização de imagem.

**Comentários**

Os comentários podem ser incorporados nas sequências de solicitação em qualquer lugar e são identificados por um ponto final (.) logo após o separador de comandos (&amp;). O comentário é encerrado pela próxima ocorrência de um separador de comando (não codificado). Esse recurso pode ser usado para adicionar informações à solicitação do que não são para uso do Servidor de imagens, como carimbos de data e hora e IDs de banco de dados.

**Decodificação HTTP**

Primeiras extrações de renderização de imagem *`object`* e *`modifiers`* da solicitação recebida. A variável *`object`* O é separado em elementos de caminho que são decodificados individualmente por HTTP. A variável *`modifiers`* a sequência de caracteres é separada em *`command`*= *`value`* pares e *`value`* é então decodificado por HTTP antes do processamento específico do comando.
