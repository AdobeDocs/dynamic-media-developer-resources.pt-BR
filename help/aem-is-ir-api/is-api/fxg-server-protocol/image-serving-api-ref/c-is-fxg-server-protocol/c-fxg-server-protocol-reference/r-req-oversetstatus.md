---
title: solic
description: Tipo de solicitação. Especifica o tipo de solicitação.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 0%

---

# solic{#req}

Tipo de solicitação. Especifica o tipo de solicitação.

`req={validate|contents|oversetstatus|exists}`

<table id="table_F39239E5244746DB9F253BB0D5E85D54"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Valor </th> 
   <th colname="col2" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> validar</span> </p> </td> 
   <td colname="col2"> <p> Retorna quaisquer erros na renderização do fxg com os modificadores de url fornecidos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> conteúdo</span> </p> </td> 
   <td colname="col2"> <p> Retorna a lista xml de todos os elementos com um valor de atributo <span class="codeph"> s7:element</span> e uma lista de todas as páginas no documento fxg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Retorna uma lista XML com os elementos <span class="codeph"> &lt;RichText/&gt;</span> com excesso de tipos. </p> <p>Retorna uma lista xml de elementos <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> com excesso de tipos para processamento no lado do cliente. Apenas <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> elementos com excesso de tipos são retornados. O <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> é um atributo <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> necessário ao usar <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Nenhum elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> com excesso de tipos sem <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> está listado. Cada elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> da lista tem o <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> e a caixa delimitadora do quadro de texto com excesso de tipos. O atributo <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> indica o índice de texto na matéria até a qual o texto pôde caber no quadro. O <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> se aplica somente aos elementos <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> no FXG solicitado. Ele não lista nenhum elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> de nenhum FXG inserido. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> existe</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>identificador de solicitação exclusivo do reqId </p> <p>Retorna uma única propriedade chamada catalogRecord.exists. O valor da propriedade é definido como "1" se a entrada do catálogo especificado existir na imagem ou no catálogo padrão, caso contrário, é definido como "0". req=exists solicitações em relação ao contexto /is/content indica a presença ou a ausência de um registro especificado no catálogo de conteúdo estático. </p> </td> 
  </tr> 
 </tbody> 
</table>
