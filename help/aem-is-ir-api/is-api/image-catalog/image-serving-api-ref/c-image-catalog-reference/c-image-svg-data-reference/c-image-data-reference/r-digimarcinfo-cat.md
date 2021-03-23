---
description: Informações da imagem da Digimarc. Habilita a incorporação da Digimarc e especifica o tipo de marca d'água e quaisquer dados específicos da imagem associados.
seo-description: Informações da imagem da Digimarc. Habilita a incorporação da Digimarc e especifica o tipo de marca d'água e quaisquer dados específicos da imagem associados.
seo-title: DigimarcInfo
solution: Experience Manager
title: DigimarcInfo
uuid: 8371880e-47df-4333-b8a6-91feaf16c409
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 7%

---


# DigimarcInfo{#digimarcinfo}

Informações da imagem da Digimarc. Habilita a incorporação da Digimarc e especifica o tipo de marca d&#39;água e quaisquer dados específicos da imagem associados.

## Propriedades {#section-62af219e8bac422b8541841221c9ce4f}

Quatro valores inteiros, separados por vírgulas.

`*``*, *``*, *`typeflagsval1`*, *`val2`*`

`*`O tipo `*` ativa a incorporação do Digimarc e especifica o tipo de marca d&#39;água:

<table id="table_3648951F14D94C5BAD097CFB783F1EE7"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><b>Tipo de marca d'água</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Nenhum. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Básico. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>ID da imagem. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>1</b> </p> </td> 
   <td> <p>ID da transação. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Anos de direitos autorais. </p> </td> 
  </tr> 
 </tbody> 
</table>

`*``*` sinaliza um campo de bits com três valores. Defina bit 0 para indicar conteúdo protegido por cópia, bit 1 para indicar conteúdo restrito e bit 2 para indicar conteúdo adulto:

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
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Protegido por cópia. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>2</b> </p> </td> 
   <td> <p>Restrito. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
   <td> <p>Protegido por cópia, restrito. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>4</b> </p> </td> 
   <td> <p>Conteúdo maduro. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>5</b> </p> </td> 
   <td> <p>Copie conteúdo protegido e adulto. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>6</b> </p> </td> 
   <td> <p>Conteúdo restrito de adultos. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>7</b> </p> </td> 
   <td> <p>Conteúdo protegido por cópia, restrito e maduro. </p> </td> 
  </tr> 
 </tbody> 
</table>

A interpretação de `*`val1`*` e `*`val2`*` depende de `*`type`*`:

<table id="table_6B29F76BC1974C12AB7124BF84B29EC2"> 
 <thead> 
  <tr> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> type</span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val1  </span> </span> </p> </th> 
   <th class="entry"> <p><span class="codeph"> <span class="varname"> val2  </span> </span> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>0</b> </p> </td> 
   <td> <p>Não usado. </p> </td> 
   <td> <p>Não usado. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>3</b> </p> </td> 
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

Herdado do atributo::DigimarcInfo se o campo não estiver presente ou se estiver vazio.

## Exemplos {#section-0f14727a0a2a408781c9df71fed7f42d}

&quot;0,0,0,0&quot; desativa a marca d&#39;água Digimarc para esta imagem.

&quot;1,5,0,0&quot; especifica uma marca d&#39;água básica com o sinalizador de conteúdo adulto e protegido por cópia definido.

&quot;2,0,4567,0&quot; especifica uma marca d&#39;água com uma ID de imagem.

&quot;3,2,56483,0&quot; especifica uma marca d&#39;água com uma ID de transação e o sinalizador de conteúdo restrito definido.

&quot;4,0,1998,2001&quot; especifica uma marca d&#39;água com anos de direitos autorais.

## Consulte também {#section-4bd3e7272c5c4b8cb8c5ca1ac7ed1012}

[atributo::DigimarcInfo](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcinfo.md#reference-de88636cb9b4435a94e3d0a80f072667) ,  [atributo::DigimarcId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-digimarcid.md#reference-33e3eca7f1874510904e5c8645cecd68)
