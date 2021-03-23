---
description: Remove as permissões da pasta.
seo-description: Remove as permissões da pasta.
seo-title: removeFolderPermissions
solution: Experience Manager
title: removeFolderPermissions
uuid: cd9f7a42-e314-4ec9-abe2-a27581c7cd23
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# removeFolderPermissions{#removefolderpermissions}

Remove as permissões da pasta.

Sintaxe

## Tipos de usuário autorizados {#section-bfa745624f9b43aaba6c226ac6700fe7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-7efa68377fd846219b906d354ae64ed3}

**Entrada (removeFolderPermissionsParam)**

<table id="table_15223256C63C4F008BDB1DF6F0AFE6A8"> 
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
   <td colname="col3"> Sim </td> 
   <td colname="col4"> O identificador para a empresa com pastas com permissões que você deseja remover. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> folderHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Lide com a pasta . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateChildren</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> <p>Quando <span class="codeph"> true</span>: 
     <ul id="ul_1305D060E0F34A61AA3C827E43F296E6"> 
      <li id="li_AB8705F3CEAD4B8A8F1C28291A6F7EC8">A remoção de permissões se propaga por meio de todas as operações de permissão da pasta. </li> 
     </ul> </p> <p>Quando <span class="codeph"> false</span>: 
     <ul id="ul_19AEE80F1FC84B64AD623E050C12A0CD"> 
      <li id="li_B8B78851004C43DB8CB7958E380AF510">A operação afeta somente a pasta especificada. </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (removeFolderPermissionsReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-04390f0ec7cc460cb5d34d518e33e7a5}

Essa amostra de código remove permissões de uma pasta e suas subpastas. Defina `updateChildren` como `false` se precisar remover permissões somente da pasta pai.

**Solicitação**

```java
<removeFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <updateChildren>true</updateChildren>
</removeFolderPermissionsParam>
```

**Resposta**

Nenhum.
