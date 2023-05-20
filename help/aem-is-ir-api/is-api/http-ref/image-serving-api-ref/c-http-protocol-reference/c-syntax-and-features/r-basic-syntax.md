---
description: 'A sintaxe básica do protocolo HTTP é a seguinte:'
solution: Experience Manager
title: Sintaxe básica do protocolo HTTP do Servidor de imagens
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---

# Sintaxe básica do protocolo HTTP do Servidor de imagens{#image-serving-http-protocol-basic-syntax}

A sintaxe básica do protocolo HTTP é a seguinte:

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> solicitação</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> objeto</span>][?<span class="varname"> modificadores</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> server </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> porta</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> objeto</span> </span> </p></td> 
  <td class="stentry"> <p>Especificador de objeto de origem (caminho da imagem ou entrada do catálogo de imagens). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificadores</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificador</span>*[&amp;<span class="varname"> modificador</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificador</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">comando|{$<span class="varname"> macro</span>$}|{.<span class="varname"> comentário</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> comando</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}}[=<span class="varname"> value</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
  <td class="stentry"> <p>Nome de uma macro de comando.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> comentário</span> </span> </p></td> 
  <td class="stentry"> <p>Sequência de comentários (ignorada pelo servidor).</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>Um dos nomes de comando ou atributo compatíveis.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>Nome de uma variável personalizada.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span> </span> </p></td> 
  <td class="stentry"> <p>Valor do comando ou da variável. </p></td> 
 </tr> 
</table>

*`server_address`*, *`cmdName`*, *`macro`*, e *`var`* não diferenciam maiúsculas de minúsculas. O servidor preserva as letras maiúsculas e minúsculas de todos os outros valores de string.

*`value`* é específico do comando e pode consistir em um ou mais valores separados por vírgulas. Consulte a descrição dos comandos individuais para obter detalhes.

## Identificador do servidor {#section-926ae55ddba14b8d952147a5fd701e14}

A variável [!DNL /is/image] O contexto raiz é necessário para todas as solicitações HTTP para o Servidor de imagens.

## Decodificação HTTP {#section-20922baccd804d2d986b44ce9a183a7d}

Primeiros extratos do Servidor de imagens *`object`* e *`modifiers`* da solicitação recebida. *`object`* O é separado em elementos de caminho que são decodificados individualmente por HTTP. A variável *`modifiers`* a sequência de caracteres é separada em *`command`*= *`value`* pares e *`value`* é então decodificado por HTTP antes do processamento específico do comando.

>[!NOTE]
>
>A menos que seja indicado de outra forma na documentação, todos os caracteres inseguros devem ser codificados de acordo com o padrão HTTP. Consulte a especificação HTTP para obter detalhes.

## Comentários {#section-69ef0be0f17a418c87a0eba21c2ddb00}

Os comentários podem ser incorporados nas cadeias de caracteres de solicitação em qualquer lugar e são identificados por um ponto (.) logo após o comando separator(&amp;). O comentário é encerrado pela próxima ocorrência de um separador de comando (não codificado). Esse recurso pode ser usado para adicionar informações à solicitação do, que não são para uso do Servidor de imagens, como carimbos de data e hora e IDs de banco de dados.

## Consulte também {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Tipos de dados](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa), [Especificação HTTP/1.1](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
