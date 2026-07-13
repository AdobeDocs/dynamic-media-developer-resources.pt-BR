---
description: Valores válidos para os campos PropertySetType e createPropertySetTypeParam.
solution: Experience Manager
title: PropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f0c51e67-6927-4b9f-9935-222e6a194c13
TQID: 'https://experienceleague.adobe.com/yZz7rkrq0rzrrmSH-Wmza-LFExg23GcBp9MKc25wcrE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 0%

---

# [!DNL PropertySetType]{#propertysettype}

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
   <td colname="col3"> Digitar identificador. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Identificador da empresa. <p>Observação: o tipo será global se o identificador da empresa não estiver presente. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nome</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Digite o nome. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> propertyType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Um dos Tipos de conjunto de propriedades. Consulte a Entrada (<span class="codeph"> createPropertySetTypeParam</span>). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> allowMultiple</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> Se permitir que várias instâncias de conjuntos de propriedades sejam anexadas a um objeto para esse tipo. </td> 
  </tr> 
 </tbody> 
</table>

