---
title: DigimarcInfo
description: Informações da imagem da Digimarc. Habilita a incorporação da Digimarc e especifica o tipo de marca d'água e quaisquer dados específicos da imagem associados.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 87f4d8f0-02b9-4511-9151-89c58116c78d
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# DigimarcInfo{#digimarcinfo}

Informações da imagem da Digimarc. Habilita a incorporação da Digimarc e especifica o tipo de marca d&#39;água e quaisquer dados específicos da imagem associados.

## Propriedades {#section-62af219e8bac422b8541841221c9ce4f}

Quatro valores inteiros, separados por vírgulas.

`*`tipo`*, *`sinalizadores`*, *`val1`*, *`val2`*`

`*`type`*` habilita a incorporação de Digimarc e especifica o tipo de marca d&#39;água:

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> tipo</span> </span> </p> </th> 
   <th class="entry"> <p><b>Tipo de Marca D'Água</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Nenhum. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Básico. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>ID da imagem. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>ID da transação. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Anos de copyright. </p> </td> 
  </tr> 
 </tbody> 
</table>

`*`sinalizadores`*` é um campo de bits com três valores. Defina o bit 0 para indicar conteúdo protegido contra cópia, o bit 1 para indicar conteúdo restrito e o bit 2 para indicar conteúdo adulto:

<table id="table_00F218515FBE484F9D05CBAF14F9D045"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> sinalizadores</span> </span> </p> </th> 
   <th class="entry"> <p><b>Descrição</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>- </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Protegido contra cópia. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Restrito. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Protegido contra cópia, restrito. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Conteúdo maduro. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>Conteúdo adulto protegido contra cópia. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>Conteúdo adulto restrito. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>Conteúdo maduro, restrito e protegido contra cópia. </p> </td> 
  </tr> 
 </tbody> 
</table>

A interpretação de `*`val1`*` e `*`val2`*` depende do `*`tipo`*`:

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> tipo</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1 </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2 </span> </span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Não usado. </p> </td> 
   <td> <p>Não usado. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>Não usado. </p> </td> 
   <td> <p>Não usado. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>ID da imagem. </p> </td> 
   <td> <p>Não usado. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>ID da transação. </p> </td> 
   <td> <p>Não usado. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Primeiro ano de copyright. </p> </td> 
   <td> <p>Segundo ano de copyright. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Padrão {#section-4bb97e5f79074be89cc691e73449eb43}

Herdado de attribute::DigimarcInfo se o campo não estiver presente ou se estiver vazio.

## Exemplos {#section-0f14727a0a2a408781c9df71fed7f42d}

&quot;0,0,0,0&quot; desativa a marca d&#39;água da Digimarc para esta imagem.

&quot;1,5,0,0&quot; especifica uma marca d&#39;água básica com o sinalizador de conteúdo para adulto e protegido contra cópia definido.

&quot;2,0,4567,0&quot; especifica uma marca d&#39;água com uma ID de imagem.

&quot;3,2,56483,0&quot; especifica uma marca d&#39;água com uma ID de transação e o sinalizador de conteúdo restrito definido.

&quot;4,0,1998,2001&quot; especifica uma marca d&#39;água com anos de copyright.

## Consulte também {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[attribute::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) , [attribute::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
