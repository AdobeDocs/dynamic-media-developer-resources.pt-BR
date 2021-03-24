---
description: Define a lista de ativos associados a um conjunto de imagens.
solution: Experience Manager
title: setImageSetMembers
feature: Dynamic Media Classic, SDK/API, Conjuntos de imagens
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# setImageSetMembers{#setimagesetmembers}

Define a lista de ativos associados a um conjunto de imagens.

Esta operação ignora o parâmetro `pageReset` para `ImageSets` e `SpinSets` e força o valor a true.

## Tipos de usuário autorizados {#section-8968d6a39a344cfc8521020d92ae8916}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura e gravação ao ativo do conjunto de imagens e acesso de leitura a cada ativo do membro.

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
   <td colname="col4"> <p>Manuseio da empresa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Identificador do conjunto de imagens. </td> 
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
