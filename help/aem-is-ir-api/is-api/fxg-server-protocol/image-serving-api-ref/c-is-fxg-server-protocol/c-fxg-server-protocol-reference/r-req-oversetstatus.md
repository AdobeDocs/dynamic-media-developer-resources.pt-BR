---
description: Tipo de solicitação. Especifica o tipo de solicitação.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# req{#req}

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
   <td colname="col1"> <p> <span class="codeph"> validate</span> </p> </td> 
   <td colname="col2"> <p> Retorna quaisquer erros ao renderizar o fxg com os modificadores de url fornecidos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> conteúdo</span> </p> </td> 
   <td colname="col2"> <p> Retornar a lista xml de todos os elementos com um <span class="codeph"> s7:element</span> e uma lista de todas as páginas no documento fxg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Retorna a lista XML da qual <span class="codeph"> &lt;richtext /&gt;</span> Os elementos do são sobrepostos. </p> <p>Retorna uma lista xml de <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementos com excesso para processamento no lado do cliente. Somente <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> os elementos com excesso são retornados. <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> é obrigatório <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> ao usar <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Qualquer excedente <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementos sem um <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> não está listado. Cada <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> na lista tem a variável <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>e a caixa delimitadora do quadro de texto com excesso. O <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> indica o índice de texto na história até a qual o texto foi capaz de se ajustar no quadro. <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> só se aplica a <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> no FXG solicitado. Não listará nenhum <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementos de qualquer FXGs incorporado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> existe</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>identificador de solicitação exclusiva reqId </p> <p>Retorna uma única propriedade chamada catalogRecord.exists. O valor da propriedade é definido como "1" se a entrada de catálogo especificada existir na imagem ou no catálogo padrão, caso contrário, é definido como "0". as solicitações req=exists no contexto /is/content indicarão a presença ou ausência de um registro especificado no catálogo de conteúdo estático. </p> </td> 
  </tr> 
 </tbody> 
</table>
