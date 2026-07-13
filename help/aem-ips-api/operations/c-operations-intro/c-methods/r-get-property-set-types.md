---
description: Obtém os tipos de conjunto de propriedades associados à empresa especificada ou os tipos de conjunto de propriedades globais se nenhuma empresa for especificada.
solution: Experience Manager
title: getPropertySetTypes
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7686d30b-e071-4950-8af1-4dd25312ce4b
TQID: 'https://experienceleague.adobe.com/SNlzriBYIP3gHh5Pmgkzrw6M8Dd649uo-1pAUHiGOpA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# getPropertySetTypes{#getpropertysettypes}

Obtém os tipos de conjunto de propriedades associados à empresa especificada ou os tipos de conjunto de propriedades globais se nenhuma empresa for especificada.

Sintaxe

## Tipos de usuário autorizados {#section-9c7c0d2cd2c94dfca3f96774b3a9a2c6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-ac3ed9e036b54ea993f544046ff0e15d}

**Entrada (getPropertySetTypesParam)**

<table id="table_2590368FEEF04AD4B074412CBBA90F88"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obrigatório </th> 
   <th colname="col4" class="entry"> Descrição </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4">O identificador da empresa à qual os tipos de conjunto de propriedades estão associados. <p>Omita se quiser retornar tipos de conjunto de propriedades globais. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (getPropertySetTypesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| typeArray | `types:PropertySetTypeArray` | Sim | Uma matriz de tipos de conjuntos de propriedades associados à empresa especificada ou os tipos de conjuntos de propriedades globais se nenhuma empresa tiver sido especificada. |

## Exemplos {#section-280c406a90864409856aee44d4069a52}

**Solicitação**

```java
<getPropertySetTypesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <companyHandle>c|1</companyHandle>
</getPropertySetTypesParam>
```

**Resposta**

```java
<getPropertySetTypesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
  <typeArray>
    <items>
      <typeHandle>pt|1</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>SavedSearch</name>
      <propertyType>UserCompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
    <items>
      <typeHandle>pt|2</typeHandle>
      <companyHandle>c|1</companyHandle>
      <name>CompanyMetadata</name>
      <propertyType>CompanyProperty</propertyType>
      <alllowMultiple>true</alllowMultiple>
    </items>
  </typeArray>
</getPropertySetTypesReturn>
```

