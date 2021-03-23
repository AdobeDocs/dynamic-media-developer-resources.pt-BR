---
description: Retorna informações sobre a empresa especificada, incluindo o identificador da empresa, o nome da empresa, o caminho raiz e a data de expiração. Você deve especificar companyHandle ou companyName cujas informações deseja recuperar.
seo-description: Retorna informações sobre a empresa especificada, incluindo o identificador da empresa, o nome da empresa, o caminho raiz e a data de expiração. Você deve especificar companyHandle ou companyName cujas informações deseja recuperar.
seo-title: getCompanyInfo
solution: Experience Manager
title: getCompanyInfo
uuid: 9218cba8-2873-46b7-90e3-7ab9d5018690
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---


# getCompanyInfo{#getcompanyinfo}

Retorna informações sobre a empresa especificada, incluindo o identificador da empresa, o nome da empresa, o caminho raiz e a data de expiração. Você deve especificar companyHandle ou companyName cujas informações deseja recuperar.

Sintaxe

## Tipos de usuário autorizados {#section-74f20fb8602e4f96810795bc4b6f7fdf}

* `IpsUser`
* `IpsAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-7dec8871c89a414c9f066adade1831d8}

**Entrada (getCompanyInfoParam)**

<table id="table_DD2688C9DA9F49C9ABCA24944829B3E5"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obrigatório </p> </th> 
   <th colname="col4" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> ou <span class="codeph"> <span class="varname"> companyName</span> </span> é necessário. </p> </td> 
   <td colname="col4"> <p>O identificador da empresa cujas informações você deseja obter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyName</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p><span class="codeph"> <span class="varname"> companyHandle</span> </span> ou <span class="codeph"> <span class="varname"> companyName</span> </span> é necessário. </p> </td> 
   <td colname="col4"> <p>O nome da empresa cujas informações você deseja obter. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (getCompanyInfoReturn)**

<table id="table_634D4E274BA7494C9C917FD244286F0D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nome </p> </th> 
   <th colname="col2" class="entry"> <p>Tipo </p> </th> 
   <th colname="col3" class="entry"> <p>Obrigatório </p> </th> 
   <th colname="col4" class="entry"> <p>Descrição </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> companyInfo</span> </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> tipos:Empresa</span> </p> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Manipule e outras informações descritivas sobre a empresa. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplos {#section-3d5342aa7cb34b1fa84d7dea6e16e4aa}

Esta amostra de código retorna todas as informações sobre uma empresa usando um nome e identificador da empresa. Ele retorna dados semelhantes à resposta recebida ao criar uma empresa.

**Solicitação**

```java
<ns1:getCompanyInfoParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyName>Planetary</ns1:companyName>
</ns1:getCompanyInfoParam>
```

**Resposta**

```java
<ns1:getCompanyInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyInfo>
      <ns1:companyHandle>137</ns1:companyHandle>
      <ns1:name>Planetary</ns1:name>
      <ns1:rootPath>Planetary/</ns1:rootPath>
      <ns1:expires>2101-01-31T23:00:00.030Z</ns1:expires>
   </ns1:companyInfo>
</ns1:getCompanyInfoReturn>
```

