---
title: Sintaxe básica do protocolo HTTP de renderização de imagem
description: Esta seção descreve a sintaxe básica do protocolo HTTP de renderização de imagem do Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8bf5920a-7ada-4db5-9796-05c5a17532c8
TQID: 'https://experienceleague.adobe.com/v-ucFAnnoq6ywaB97QSXodqnO4VWFvaK6I2HJ2-a4Fc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 227
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
   <td colname="col2"> <p>http://<span class="varname"> server</span>/ir/render[/<span class="varname"> vignette</span> ] [ ?<span class="varname"> modificadores</span> ] </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="varname"> servidor </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> endereço_servidor</span> [ :<span class="varname"> porta</span> ] </p> </td> 
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
   <td colname="col2"> <p>&lbrace; <span class="varname"> cmdName</span> | { $<span class="varname"> var</span> } [ = <span class="varname"> value</span> ] </p> </td> 
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
   <td colname="col1"> <p><span class="varname"> valor </span> </p> </td> 
   <td colname="col2"> <p>Valor do comando ou da variável. </p> </td> 
  </tr> 
 </tbody> 
</table>

*`server`*, *`cmdName`*, *`macro`* e *`var`* não diferenciam maiúsculas de minúsculas. O servidor preserva as letras maiúsculas e minúsculas de todos os outros valores de string.

**Identificador do servidor**

O contexto raiz &#39; `/ir/render`&#39; é necessário para todas as solicitações HTTP para a Renderização de Imagem.

**Comentários**

Os comentários podem ser incorporados nas sequências de solicitação em qualquer lugar e são identificados por um ponto final (.) logo após o separador de comandos (&amp;). O comentário é encerrado pela próxima ocorrência de um separador de comando (não codificado). Esse recurso pode ser usado para adicionar informações à solicitação do que não são para uso do Servidor de imagens, como carimbos de data e hora e IDs de banco de dados.

**Decodificação HTTP**

A Renderização de Imagem primeiro extrai *`object`* e *`modifiers`* da solicitação de entrada. O *`object`* é então separado em elementos de caminho que são decodificados individualmente por HTTP. A cadeia de caracteres *`modifiers`* é separada em *`command`*= *`value`* pares e *`value`* é então decodificado em HTTP antes do processamento específico do comando.

