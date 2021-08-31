---
description: Os valores de comando devem ser codificados em http usando %xx sequências de escape, de modo que as sequências de valor não incluam os caracteres reservados '=', '&' e '%'.
solution: Experience Manager
title: Codificação HTTP do Image Serving
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: aec8463f-f72a-4203-89ab-8a4f0ad9d6f9
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 21%

---

# Codificação HTTP do Image Serving{#image-serving-http-encoding}

Os valores de comando devem ser codificados em http usando %xx sequências de escape, de modo que as sequências de valor não incluam os caracteres reservados &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39;.

Caso contrário, as regras de codificação HTTP padrão se aplicam. A especificação HTTP requer a codificação dos caracteres não seguros, bem como de quaisquer caracteres de controle, como `<return>` e `<tab>`. A codificação de URL de um caractere consiste em um símbolo &quot;%&quot;, seguido pela representação hexadecimal de dois dígitos (não diferencia maiúsculas de minúsculas) do ponto de código ISO-Latino para o caractere. Os caracteres e pontos de código não seguros são:

<table id="table_D2C01CADB35E477D82D4C27586424625"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Caractere não seguro </th> 
   <th colname="col2" class="entry"> Pontos de código (hexadecimal) </th> 
   <th colname="col3" class="entry"> Pontos de código (dec) </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Espaço </p> </td> 
   <td colname="col2"> <p>20º </p> </td> 
   <td colname="col3"> <p>32º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&lt;&gt; </p> </td> 
   <td colname="col2"> <p>3C </p> </td> 
   <td colname="col3"> <p>60º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&gt; </p> </td> 
   <td colname="col2"> <p>3E </p> </td> 
   <td colname="col3"> <p>62º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>" </p> </td> 
   <td colname="col2"> <p>22º </p> </td> 
   <td colname="col3"> <p>34º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p># </p> </td> 
   <td colname="col2"> <p>23º </p> </td> 
   <td colname="col3"> <p>35º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>% </p> </td> 
   <td colname="col2"> <p>25. </p> </td> 
   <td colname="col3"> <p>37º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;lbrace; </p> </td> 
   <td colname="col2"> <p>7B </p> </td> 
   <td colname="col3"> <p>123º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;rbrace; </p> </td> 
   <td colname="col2"> <p>7D </p> </td> 
   <td colname="col3"> <p>125 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>| </p> </td> 
   <td colname="col2"> <p>7C </p> </td> 
   <td colname="col3"> <p>124 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>\ </p> </td> 
   <td colname="col2"> <p>5C </p> </td> 
   <td colname="col3"> <p>92 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>^ </p> </td> 
   <td colname="col2"> <p>5E </p> </td> 
   <td colname="col3"> <p>94 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>~ </p> </td> 
   <td colname="col2"> <p>7E </p> </td> 
   <td colname="col3"> <p>126 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;lbrack; </p> </td> 
   <td colname="col2"> <p>5B </p> </td> 
   <td colname="col3"> <p>91º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;rbrack; </p> </td> 
   <td colname="col2"> <p>5D </p> </td> 
   <td colname="col3"> <p>93 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp;grave; </p> </td> 
   <td colname="col2"> <p>60º </p> </td> 
   <td colname="col3"> <p>96 </p> </td> 
  </tr> 
 </tbody> 
</table>

Caracteres reservados também devem ser codificados.

<table id="table_A6C808A05EA6420F8125186D3D5C9E33"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Caractere reservado </th> 
   <th colname="col2" class="entry"> Pontos de código (hexadecimal) </th> 
   <th colname="col3" class="entry"> Pontos de código (Dez) </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>$ </p> </td> 
   <td colname="col2"> <p>24º </p> </td> 
   <td colname="col3"> <p>36º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>&amp; </p> </td> 
   <td colname="col2"> <p>26º </p> </td> 
   <td colname="col3"> <p>38º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>+ </p> </td> 
   <td colname="col2"> <p>2B </p> </td> 
   <td colname="col3"> <p>43º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>, </p> </td> 
   <td colname="col2"> <p>2C </p> </td> 
   <td colname="col3"> <p>44º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>/ </p> </td> 
   <td colname="col2"> <p>2F </p> </td> 
   <td colname="col3"> <p>47º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>: </p> </td> 
   <td colname="col2"> <p>3A </p> </td> 
   <td colname="col3"> <p>58º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>; </p> </td> 
   <td colname="col2"> <p>3B </p> </td> 
   <td colname="col3"> <p>59 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>= </p> </td> 
   <td colname="col2"> <p>3D </p> </td> 
   <td colname="col3"> <p>61º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>? </p> </td> 
   <td colname="col2"> <p>3F </p> </td> 
   <td colname="col3"> <p>63º </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>@ </p> </td> 
   <td colname="col2"> <p>40º </p> </td> 
   <td colname="col3"> <p>64º </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplo {#section-b85895e5b6a84b96b7fca987656dd34d}

`…&$text=rate&weight=85% 27#&…`

Se a ofuscação não for aplicada, o fragmento de solicitação acima deverá ser codificado da seguinte maneira:

`…&$text=rate%26weight%3D85%25%2027%23&…`

Se a ofuscação for aplicada, a codificação poderá ser limitada para remover os caracteres &#39;=&#39;, &#39;&amp;&#39; e &#39;%&#39;:

`…&$text=rate%26weight%3D85%25 27#&…`

## Consulte também {#section-295476ec34c74973962d07dfa9eb2180}

[Solicitar ofuscação](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-obfuscation.md#reference-895f65d6796c43bb9bad21a676ed714d), Especificação  [HTTP/1.1 (RFC 2616)](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
