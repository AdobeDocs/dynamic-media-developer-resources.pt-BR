---
description: Adiciona um usuário a uma matriz de grupos.
solution: Experience Manager
title: addGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c5b5e155-d285-4304-98bc-1d938793e2c0
TQID: 'https://experienceleague.adobe.com/E26D4T5xx58eE5G1APbIi46B-SL1BM9YqGibC1n4IVo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 92
ht-degree: 0%

---

# addGroupMembership{#addgroupmembership}

Adiciona um usuário a uma matriz de grupos.

Sintaxe

## Tipos de usuário autorizados {#section-fe950150718a474d8df30d0f4453c022}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-e250f6ddb13646808c6a8860b6442bc5}

**Entrada (addGroupMembershipParam)**

<table id="table_71AD8902E4854CA5A12379DBA4DF17C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> userHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Processe o usuário cuja associação de grupo você deseja adicionar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> groupHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:HandleArray</span> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Matriz de identificadores para os grupos aos quais você deseja que a empresa pertença. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (addGroupMembershipParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-f7a1f40c3d7a40ea964b29056c734d81}

Este exemplo adiciona um grupo a uma empresa com groupHandleArray. Este exemplo usa apenas um grupo.

**Solicitação**

```java {.line-numbers}
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**Resposta**

Nenhum.
