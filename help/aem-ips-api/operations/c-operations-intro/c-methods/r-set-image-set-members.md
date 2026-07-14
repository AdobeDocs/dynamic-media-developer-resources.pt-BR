---
description: Define a lista de ativos associados a um conjunto de imagens.
solution: Experience Manager
title: setImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: c30df5fe-e355-45d4-8c06-e396caca0d58
TQID: 'https://experienceleague.adobe.com/nacym3xe-m5gu-Hi2Gqkz-O03-CbqB9B-uCDRVkhrvc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 0%

---

# setImageSetMembers{#setimagesetmembers}

Define a lista de ativos associados a um conjunto de imagens.

Esta operação ignora o parâmetro `pageReset` para `ImageSets` e `SpinSets` e força o valor para true.

## Tipos de usuário autorizados {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura e gravação ao ativo do conjunto de imagens e acesso de leitura a cada ativo membro.

## Parâmetros {#section-2f46efcd24c648aeacba738509426e46}

**Entrada (setImageSetMembersParam)**

<table id="table_0CBBB65BCEFD4125A4069A080DFC873A"> 
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
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Identificador da empresa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Identificador de conjunto de imagens. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:ImageSetMemberUpdateArray</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Matriz de membros do ativo que pertencem ao conjunto de imagens. </td> 
  </tr> 
 </tbody> 
</table>

**Saída (setImageSetMembersReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-7b87219034464aa98524178ccee27738}

Essa amostra de código usa uma matriz de membros para definir os membros de um conjunto de imagens.

**Solicitação**

```java
<setImageSetMembersParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <assetHandle>34205|22|929</assetHandle>
   <memberArray>
      <items>
         <assetHandle>24266|1|17062</assetHandle>
         <pageReset>true</pageReset>
      </items>
   </memberArray>
</setImageSetMembersParam>
```

**Resposta**

Nenhum.

