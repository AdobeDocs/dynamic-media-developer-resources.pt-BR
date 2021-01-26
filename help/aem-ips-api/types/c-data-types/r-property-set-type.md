---
description: Valores válidos para os campos PropertySetType e createPropertySetTypeParam.
seo-description: Valores válidos para os campos PropertySetType e createPropertySetTypeParam.
seo-title: PropertySetType
solution: Experience Manager
title: PropertySetType
topic: Dynamic Media Image Production System API
uuid: 83220180-3272-4552-974d-a73e6aad3483
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# PropertySetType{#propertysettype}

Valores válidos para os campos PropertySetType e createPropertySetTypeParam.

Os valores incluem:

* `UserProperty`
* `CompanyProperty`
* `UserCompanyProperty`

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> typeHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Digite identificador. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Alça da empresa. <p>Observação:  O tipo é global se o identificador de empresa não estiver presente. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Digite o nome. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> propertyType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Um dos tipos de conjunto de propriedades. Consulte Entrada (<span class="codeph"> createPropertySetTypeParam</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> allowMultiple</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> Se é necessário permitir que várias instâncias de conjunto de propriedades sejam anexadas a um objeto para esse tipo. </td> 
  </tr> 
 </tbody> 
</table>

