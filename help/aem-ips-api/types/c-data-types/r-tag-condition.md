---
description: Define as condições de pesquisa para os campos de tags.
seo-description: Define as condições de pesquisa para os campos de tags.
seo-title: TagCondition
solution: Experience Manager
title: TagCondition
topic: Dynamic Media Image Production System API
uuid: c7727267-05b6-4011-9ddf-7f3134e9609b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---


# TagCondition{#tagcondition}

Define as condições de pesquisa para os campos de tags.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Identificador de campo de tag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Depende do tipo de campo de tag e se o campo value ou valueArray é usado. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">Se <span class="codeph"> value</span> for transmitido, <span class="codeph"> op</span> deverá ser a constante de cadeia Correspondências. A condição corresponde a qualquer ativo associado ao valor da tag. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">Se <span class="codeph"> valueArray</span> for transmitido, o campo op poderá ser a constante <span class="codeph"> MatchesAny</span> para campos de tag únicos ou com vários valores. Uma condição <span class="codeph"> MatchesAny</span> corresponde a qualquer ativo associado a pelo menos um dos valores de tag em <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">Para campos de tags de vários valores, o campo op pode ser definido como a constante <span class="codeph"> MatchesAll</span> com o campo <span class="codeph"> valueArray</span>. Nesse caso, a condição corresponde somente aos ativos associados a todos os valores de tag em <span class="codeph"> valueArray</span> (possivelmente, além de outros valores de tag). </li>
    </ul></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Um valor correspondente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> valueArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> Vários valores correspondentes. </td> 
  </tr> 
 </tbody> 
</table>

