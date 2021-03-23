---
description: Obtém os tipos de conjunto de propriedades associados com a empresa especificada ou os tipos de conjunto de propriedades global se nenhuma empresa for especificada.
seo-description: Obtém os tipos de conjunto de propriedades associados com a empresa especificada ou os tipos de conjunto de propriedades global se nenhuma empresa for especificada.
seo-title: getPropertySetTypes
solution: Experience Manager
title: getPropertySetTypes
uuid: b707344d-5571-45eb-9e37-cf0894ee81a0
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---


# getPropertySetTypes{#getpropertysettypes}

Obtém os tipos de conjunto de propriedades associados com a empresa especificada ou os tipos de conjunto de propriedades global se nenhuma empresa for especificada.

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
   <td colname="col4">O identificador da empresa à qual os tipos de conjunto de propriedades estão associados. <p>Omita se desejar retornar tipos de conjuntos de propriedades globais. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (getPropertySetTypesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`typeArray`*` | `types:PropertySetTypeArray` | Sim | Uma matriz de tipos de conjunto de propriedades associados à empresa especificada ou aos tipos de conjunto de propriedades global se nenhuma empresa foi especificada. |

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

