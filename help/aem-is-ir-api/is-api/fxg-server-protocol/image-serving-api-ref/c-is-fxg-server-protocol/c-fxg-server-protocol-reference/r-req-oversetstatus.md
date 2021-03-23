---
description: Tipo de solicitação. Especifica o tipo de solicitação.
seo-description: Tipo de solicitação. Especifica o tipo de solicitação.
seo-title: req
solution: Experience Manager
title: req
uuid: 1c8ff9c3-9f39-46a8-bd38-8e0c5ab0f548
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '257'
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
   <td colname="col2"> <p> Retorna a lista xml de todos os elementos com um valor de atributo <span class="codeph"> s7:element</span> e uma lista de todas as páginas no documento fxg. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> oversetstatus</span> </p> </td> 
   <td colname="col2"> <p>Retorna a lista XML da qual os elementos <span class="codeph"> &lt;RichText/&gt;</span> estão com excesso de definição. </p> <p>Retorna uma lista xml de elementos <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> que estão com excesso para processamento no lado do cliente. Somente os elementos <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> com excesso serão retornados. <span class="+ topic/ph pr-d/codeph codeph"> s7:</span> elementidis um  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> atributo obrigatório ao usar  <span class="+ topic/ph pr-d/codeph codeph"> req=oversetstatus</span>. Qualquer elemento com excesso de definição <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> sem um <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span> não é listado. Cada elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> na lista tem o <span class="+ topic/ph pr-d/codeph codeph"> s7:elementid</span>, <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> e a caixa delimitadora do quadro de texto com excesso de tipos. O atributo <span class="+ topic/ph pr-d/codeph codeph"> s7:endCharIndex</span> indica o índice de texto na história até o qual o texto se ajustou no quadro. <span class="+ topic/ph pr-d/codeph codeph"> Req=</span> oversetstatusonly se aplica a  <span class="+ topic/ph pr-d/codeph codeph"> &lt;richtext /&gt;</span> elementos no FXG solicitado. Ele não listará nenhum elemento <span class="+ topic/ph pr-d/codeph codeph"> &lt;RichText/&gt;</span> de nenhum FXGs incorporado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> existe</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> req=exists[,text|javascript|xml|{json[&amp;id=reqId]}]</span> </p> <p>identificador de solicitação exclusiva reqId </p> <p>Retorna uma única propriedade chamada catalogRecord.exists. O valor da propriedade é definido como "1" se a entrada de catálogo especificada existir na imagem ou no catálogo padrão, caso contrário, é definido como "0". as solicitações req=exists no contexto /is/content indicarão a presença ou ausência de um registro especificado no catálogo de conteúdo estático. </p> </td> 
  </tr> 
 </tbody> 
</table>

