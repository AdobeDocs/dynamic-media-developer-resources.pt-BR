---
description: Redefine o status de publicação de um ou mais ativos para forçar a republicação do ativo no próximo trabalho de publicação.
solution: Experience Manager
title: forceRepublishAssets
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4c75af38-4791-4f21-8d1b-4855fcdfd4b1
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 0%

---

# forceRepublishAssets{#forcerepublishassets}

Redefine o status de publicação de um ou mais ativos para forçar a republicação do ativo no próximo trabalho de publicação.

Sintaxe

## Tipos de usuário autorizados {#section-3d5a3e3afea748d69845de5c8c376448}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-fd3f4dde9e984240b6f3e6d7a8db4e78}

**Entrada (forceRepublishAssetsParam)**

<table id="table_742D67AD77554904976EC4A07A0CBC64"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Processe a empresa que contém os ativos a serem redefinidos. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> republishFiles</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Determina que os arquivos do ativo sejam republicados nos servidores de entrega. O padrão é <span class="codeph"> true</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> resyncCatalog</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Determina que os metadados do catálogo usados para veicular o ativo sejam sincronizados para garantir que seja atual. Esse parâmetro é usado para resolver condições de corrida que podem ocorrer em quase atualizações simultâneas para o mesmo registro. O padrão é <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:HandleArray</span> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Matriz de identificadores para ativos cujo status de publicação deve ser redefinido. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Saída (forceRepublishAssetsParam)**

<table id="table_78E74186669F477E9E2D837D58A789DC"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishStateUpdateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PublishStateUpdateArray</span> </td> 
   <td colname="col3"> <p>Sim </p> </td> 
   <td colname="col4"> <p>Matriz de atualizações de estado de publicação. </p> </td> 
  </tr> 
 </tbody> 
</table>
