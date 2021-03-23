---
description: Esta seção descreve a sintaxe básica do protocolo HTTP Dynamic Media Image Rendering.
seo-description: Esta seção descreve a sintaxe básica do protocolo HTTP Dynamic Media Image Rendering.
seo-title: Sintaxe básica do protocolo HTTP de renderização de imagem
solution: Experience Manager
title: Sintaxe básica do protocolo HTTP de renderização de imagem
uuid: e01314f0-6aaa-41ca-8c05-d5db3148a071
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---


# Sintaxe básica do protocolo HTTP de renderização de imagem{#image-rendering-http-protocol-basic-syntax}

Esta seção descreve a sintaxe básica do protocolo HTTP Dynamic Media Image Rendering.

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
   <td colname="col1"> <p><span class="varname"> server  </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> server_address</span> [ :<span class="varname"> port</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> vinheta  </span> </p> </td> 
   <td colname="col2"> <p>Especificador de vinheta (caminho de arquivo relativo ou entrada de catálogo de vinheta). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modificadores  </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> modificador</span> *[ &amp;  <span class="varname"> modificador</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> modifier  </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> comando</span> | { $  <span class="varname"> macro</span> $ } | { .<span class="varname"> comentário</span> } </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> comando  </span> </p> </td> 
   <td colname="col2"> <p>{ <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> valor</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> macro  </span> </p> </td> 
   <td colname="col2"> <p>Nome de uma macro de comando. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> comentário  </span> </p> </td> 
   <td colname="col2"> <p>Sequência de comentários (ignorada pelo servidor). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> cmdName  </span> </p> </td> 
   <td colname="col2"> <p>Nome de um comando ou atributo. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> var  </span> </p> </td> 
   <td colname="col2"> <p>Nome de uma variável personalizada. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> value  </span> </p> </td> 
   <td colname="col2"> <p>Valor do comando ou da variável. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*,  *`cmdName`*,  *`macro`* e  *`var`* não diferenciam maiúsculas de minúsculas. O servidor preserva as letras maiúsculas e minúsculas de todos os outros valores da string.

**Identificador do servidor**

O contexto raiz &#39; `/ir/render`&#39; é necessário para todas as solicitações HTTP para Renderização de imagem.

**Comentários**

Os comentários podem ser incorporados às cadeias de caracteres de solicitação em qualquer lugar e são identificados por um período (.) imediatamente após o separador de comando (&amp;). O comentário é encerrado pela próxima ocorrência de um separador de comando (não codificado). Esse recurso pode ser usado para adicionar informações à solicitação, o que não é para uso do Serviço de imagem, como carimbos de data e hora, IDs do banco de dados etc.

**Decodificação HTTP**

A Renderização de imagem primeiro extrai *`object`* e *`modifiers`* da solicitação de entrada. *`object`* é então separado em elementos de caminho que são decodificados individualmente por HTTP. A sequência *`modifiers`* é separada em *`command`*= *`value`* pares e *`value`* é decodificada por HTTP antes do processamento específico do comando.
