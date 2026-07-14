---
description: Move vários ativos independentemente uns dos outros. Isso é feito por meio do tipo AssetMove contido no assetMoveArray. Cada campo AssetMove contém uma pasta de destino.
solution: Experience Manager
title: moveAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: e5bb2188-d262-4324-9f71-68634b6af654
TQID: 'https://experienceleague.adobe.com/zrKcnSbPFbQhujXvLkBkao6tYgGHcIZ-Yl2CUkj-usc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 202
ht-degree: 0%

---

# moveAssets{#moveassets}

Move vários ativos independentemente uns dos outros. Isso é feito por meio do tipo AssetMove contido no assetMoveArray. Cada campo AssetMove contém uma pasta de destino.

Sintaxe

## Tipos de usuário autorizados {#section-4166515fd9d8487b8af37465ce61802b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-7d47f663474b41cc83439288ac133cc5}

**Entrada (moveAssetsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa com os ativos a serem movidos. |
| assetMoveArray | `types:AssetMoveArray` | Sim | Uma matriz de movimentação de ativo. Ele contém um ativo e uma pasta de destino de ativo. |

**Saída (moveAssetsReturn)**

<table id="table_FD902FAB4F98413C8A051270ADD7D9C7"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> successCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Contagem de ativos movida com sucesso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Contagem de ativos que geraram avisos quando a operação tentou movê-los. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorCount</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Contagem de ativos que geraram erros quando a operação tentou movê-los. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> warningDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaults</span>que contêm: 
    <ul id="ul_689F4A87A68140F18DFB43868226A409"> 
     <li id="li_274C8BF5932F4AF584AA92F25E0F33C6">Assets que emitiu os avisos. </li> 
     <li id="li_5CC4A9120CA94F968CAF0D0135C49E0A">Códigos de aviso. </li> 
     <li id="li_AEC91FA68B2E43BC8BAA108C743F5667">Motivo do aviso. </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> errorDetailArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:AssetOperationFaultArray</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <span class="codeph"> AssetOperationFaults</span>que contêm: 
    <ul id="ul_C397BC384A134F429D01ADA28DF2E097"> 
     <li id="li_EAEBB5F539164480BA9EAA7C8FFBF69A">Assets que emitiu os erros. </li> 
     <li id="li_F96D5FBB2F7A402AA36D8DFA3971391D">Códigos de erro. </li> 
     <li id="li_F610415E416F43DDA4B1DBF1897E2F61">Motivo dos erros. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplos {#section-c31ed4c004ab4b3fa42c96d26ceb5ce7}

Esta amostra de código move ativos para um local específico especificado pelo `assetMoveArray`. A matriz inclui o identificador do ativo e o identificador da pasta. A resposta indica que os ativos foram movidos com êxito.

**Solicitação**

```java
<moveAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetMoveArray>
      <items>
          <assetHandle>a|942|1|579</assetHandle>
          <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
      <items>
         <assetHandle>a|943|1|580</assetHandle>
         <folderHandle>ApiTestCo/uploads/</folderHandle>
      </items>
   </assetMoveArray>
</moveAssetsParam>
```

**Resposta**

```java
<moveAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</moveAssetsReturn>
```

