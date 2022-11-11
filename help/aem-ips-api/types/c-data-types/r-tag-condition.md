---
description: Define condições de pesquisa para campos de tag.
solution: Experience Manager
title: TagCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ab1ac4b3-e91e-4c42-8b77-6e4c1d129b1a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 0%

---

# [!DNL TagCondition]{#tagcondition}

Define condições de pesquisa para campos de tag.

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
   <td colname="col3">Depende do tipo de campo de tag e se o valor ou o campo valueArray é usado. 
    <ul id="ul_CC0926425B094B3BB7D70CB392DBDABD">
     <li id="li_09AB923A9A8D4A71917CF59C150E4EF5">If <span class="codeph"> value</span> for aprovado, <span class="codeph"> op</span> deve ser a constante de string Correspondências. A condição corresponde a qualquer ativo associado ao valor da tag. </li>
     <li id="li_70F18494AB6C454EB611F51F16C19FAD">If <span class="codeph"> valueArray</span> for transmitido, o campo op poderá ser a constante <span class="codeph"> MatchesAny</span> para campos de tags individuais ou com vários valores. A <span class="codeph"> MatchesAny</span> corresponde a qualquer ativo associado a pelo menos um dos valores de tag em <span class="codeph"> valueArray</span>. </li>
     <li id="li_0B25542D7E964B26B15591C45D5C66D0">Para campos de tags de vários valores, o campo superior pode ser definido como a constante <span class="codeph"> MatchesAll</span> com o <span class="codeph"> valueArray</span> campo. Nesse caso, a condição só corresponde aos ativos que estão associados a todos os valores de tag em <span class="codeph"> valueArray</span> (possivelmente além de outros valores de tag). </li>
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
