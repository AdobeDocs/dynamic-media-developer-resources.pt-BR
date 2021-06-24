---
description: Obtém todos os usuários em um array.
solution: Experience Manager
title: getAllUsers
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: db1fd5c9-80f5-463a-870f-be3e38c21bab
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# getAllUsers{#getallusers}

Obtém todos os usuários em um array.

Sintaxe

## Tipos de usuário autorizados {#section-68ed5f5fcc5348308dfe074c590caeaa}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-f092ca72f2024d66a1cec690aeab870a}

**Entrada (getAllUsersParam)**

<table id="table_1FE6DDADBD134E6D8BD4B52F1EAD2E85"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeInvalid</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4">Defina como: 
    <ul id="ul_FB9F59A8293B4CCA98E42EBF8412C77B"> 
     <li id="li_3C2E6C4D3478411FA1A34D5CBFFC8108"><span class="codeph"> </span> para incluir usuários inválidos. </li> 
     <li id="li_7FCA0DE4BE2248A690076FEC6854F5CE"><span class="codeph"> </span> falsa ao omitir usuários inválidos. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (getAllUsersReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`userArray`*` | `types:UserArray` | Sim | Matriz de todos os usuários. |
| `*`Frase do código`*` | `Code Phrase` |  |  |

## Exemplos {#section-9c9a2d335513478da20652c1b1443731}

Essa amostra de código retorna todos os usuários. A resposta é truncada por brevidade.

**Solicitação**

```java
<ns1:getAllUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
</ns1:getAllUsersParam>
```

**Resposta**

```java
<ns1:getAllUsersReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userArray>
      <ns1:items>
         <ns1:userHandle>201|agentshadi@hotmail.com</ns1:userHandle>
         <ns1:firstName>333</ns1:firstName>
         <ns1:lastName>333</ns1:lastName>
         <ns1:email>my_email@someaddress.com</ns1:email>
         <ns1:role>TrialSiteUser</ns1:role>
         <ns1:isValid>true</ns1:isValid>
         <ns1:passwordExpires>2006-12-29T04:19:43.039Z</ns1:passwordExpires>
      </ns1:items>
   ...
   </ns1:userArray>
<ns1:getAllUsersReturn>
```
