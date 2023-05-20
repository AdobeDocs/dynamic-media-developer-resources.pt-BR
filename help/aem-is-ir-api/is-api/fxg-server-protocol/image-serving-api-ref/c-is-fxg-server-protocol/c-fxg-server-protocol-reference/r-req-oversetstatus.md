---
description: Tipo de solicitação. Especifica o tipo de solicitação.
solution: Experience Manager
title: solic
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9242c873-5a85-4ede-82b6-4ef15feecf50
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '240'
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
   <td colname="col2"> <p> Retorna a lista xml de todos os elementos com um <span class="codeph"> s7:elemento</span> valor do atributo e uma lista de todas as páginas no documento fxg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Retorna a lista XML da qual <span class="codeph"> &lt;richtext /&gt;</span> os elementos estão com excesso de tipos. </p> <p>Retorna uma lista xml de <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementos com excesso de tipos para processamento no cliente. Somente <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> os elementos com excesso de tipos são retornados. <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> é obrigatório <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> atributo ao usar <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Qualquer excesso <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementos sem um <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> não está listado. Each <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> o elemento na lista tem o <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span>e a caixa delimitadora do quadro de texto com excesso de tipos. A variável <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> atributo indica o índice de texto na matéria até o qual o texto pôde ser ajustado no quadro. <span class="+ topic/ph pr-d/codeph codeph"> Req=oversetstatus</span> aplica-se somente a <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementos no FXG solicitado. Ele não listará nenhum <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementos de qualquer FXG incorporado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> existe</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>identificador de solicitação exclusivo do reqId </p> <p>Retorna uma única propriedade chamada catalogRecord.exists. O valor da propriedade é definido como "1" se a entrada do catálogo especificado existir na imagem ou no catálogo padrão, caso contrário, é definido como "0". As solicitações req=exists no contexto /is/content indicarão a presença ou a ausência de um registro especificado no catálogo de conteúdo estático. </p> </td> 
  </tr> 
 </tbody> 
</table>
