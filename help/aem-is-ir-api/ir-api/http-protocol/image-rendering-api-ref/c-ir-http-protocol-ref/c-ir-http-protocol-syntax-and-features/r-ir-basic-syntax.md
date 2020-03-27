---
description: Esta seção descreve a sintaxe básica do protocolo HTTP Scene7 Image Rendering.
seo-description: Esta seção descreve a sintaxe básica do protocolo HTTP Scene7 Image Rendering.
seo-title: Sintaxe básica do protocolo HTTP de renderização de imagem
solution: Experience Manager
title: Sintaxe básica do protocolo HTTP de renderização de imagem
topic: Scene7 Image Serving - Image Rendering API
uuid: e01314f0-6aaa-41ca-8c05-d5db3148a071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Sintaxe básica do protocolo HTTP de renderização de imagem{#image-rendering-http-protocol-basic-syntax}

Esta seção descreve a sintaxe básica do protocolo HTTP Scene7 Image Rendering.

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
   <td colname="col2"> <p>Especificador de vinheta (caminho de arquivo relativo ou entrada do catálogo de vinheta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificadores </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modifier</span> *[ &amp; <span class="varname"> modifier</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificador </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> comando</span> | { $ <span class="varname"> macro</span> $ }| { .<span class="varname"> comment</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> comando </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } } [ = <span class="varname"> valor</span> ] </p> </td> 
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
   <td colname="col2"> <p>Valor do comando ou variável. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`* e *`var`* não fazem distinção entre maiúsculas e minúsculas. O servidor preserva as letras maiúsculas e minúsculas de todos os outros valores de string.

**Identificador do servidor**

O contexto raiz &#39; `/ir/render`&#39; é necessário para todas as solicitações HTTP para renderização de imagem.

**Comentários**

Os comentários podem ser incorporados às strings de solicitação em qualquer lugar e são identificados por um ponto (.) imediatamente após o separador de comando (&amp;). O comentário é encerrado pela próxima ocorrência de um separador de comando (não codificado). Esse recurso pode ser usado para adicionar informações à solicitação que não sejam para uso do Serviço de imagem, como carimbos de data e hora, IDs de banco de dados etc.

**Decodificação HTTP**

A Renderização de imagem primeiro extrai *`object`* e *`modifiers`* da solicitação recebida. *`object`* é então separado em elementos de caminho que são decodificados individualmente por HTTP. A *`modifiers`* string é separada em *`command`*= *`value`* pares e *`value`* é decodificada por HTTP antes do processamento específico do comando.
