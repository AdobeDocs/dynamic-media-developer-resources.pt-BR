---
description: Obtém os tipos de conjunto de propriedades associados à empresa especificada, ou tipos de conjunto de propriedades globais se nenhuma empresa for especificada.
seo-description: Obtém os tipos de conjunto de propriedades associados à empresa especificada, ou tipos de conjunto de propriedades globais se nenhuma empresa for especificada.
seo-title: getPropertySetTypes
solution: Experience Manager
title: getPropertySetTypes
topic: Dynamic Media Image Production System API
uuid: b707344d-5571-45eb-9e37-cf0894ee81a0
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# getPropertySetTypes{#getpropertysettypes}

Obtém os tipos de conjunto de propriedades associados à empresa especificada, ou tipos de conjunto de propriedades globais se nenhuma empresa for especificada.

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
   <td colname="col4">O identificador da empresa à qual os tipos de conjunto de propriedades estão associados. <p>Omitir se desejar retornar tipos de conjunto de propriedades globais. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (getPropertySetTypesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`typeArray`*` | `types:PropertySetTypeArray` | Sim | Uma matriz de tipos de conjunto de propriedades associados à empresa especificada ou os tipos de conjunto de propriedades globais se nenhuma empresa foi especificada. |

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

