---
description: Redefine o status de publicação de um ou mais ativos para forçar a republicação do ativo na próxima tarefa de publicação.
seo-description: Redefine o status de publicação de um ou mais ativos para forçar a republicação do ativo na próxima tarefa de publicação.
seo-title: forceRepublishAssets
solution: Experience Manager
title: forceRepublishAssets
topic: Scene7 Image Production System API
uuid: fd1f4ece-075c-40e3-868a-f27b9a4c3374
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# forceRepublishAssets{#forcerepublishassets}

Redefine o status de publicação de um ou mais ativos para forçar a republicação do ativo na próxima tarefa de publicação.

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
   <td colname="col4"> <p>Manuseie a empresa que contém os ativos para redefinir. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> republishFiles</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Designa que os arquivos do ativo sejam republicados nos servidores do delivery. O padrão é <span class="codeph"> true</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"> <span class="varname"> resyncCatalog</span> </span> </td> 
   <td colname="col2"><span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> <p>Não </p> </td> 
   <td colname="col4"> <p>Designa que os metadados do catálogo usados para servir o ativo são sincronizados para garantir que ele esteja atualizado. Esse parâmetro é usado para resolver condições de corrida que podem ocorrer em atualizações quase simultâneas para o mesmo registro. O padrão é <span class="codeph"> false</span>. </p> </td> 
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

