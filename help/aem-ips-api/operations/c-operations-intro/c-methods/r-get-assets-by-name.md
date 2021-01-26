---
description: Retorna ativos com base em uma matriz de nomes de ativos.
seo-description: Retorna ativos com base em uma matriz de nomes de ativos.
seo-title: getAssetsByName
solution: Experience Manager
title: getAssetsByName
topic: Dynamic Media Image Production System API
uuid: e86b3b16-ad93-4f70-9f59-b72395513c4c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# getAssetsByName{#getassetsbyname}

Retorna ativos com base em uma matriz de nomes de ativos.

Sintaxe

## Tipos de usuário autorizados {#section-754790841ea242d5ae8bedd587d7730e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Somente retorna ativos aos quais o usuário tem acesso de leitura.

## Parâmetros {#section-f64e93c127b84a29aa3bf2fdd916cca9}

**Entrada (getAssetsByNameParam)**

<table id="table_CE7B503B0E074719A523B458DF3A7286"> 
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
   <td colname="col4"> A alça da empresa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Fornece acesso como outro usuário. Disponível somente para administradores. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Usado para filtrar por um grupo específico. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> nameArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4"> Matriz de nomes de ativos a serem recuperados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Matriz de tipos de ativos permitidos para ativos recuperados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Matriz de tipos de ativos excluídos para ativos recuperados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Matriz de subtipos de ativos permitidos para ativos recuperados. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> hardSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> <p>Se <span class="codeph"> true</span> e <span class="codeph"> assetSubTypeArray</span> não estiverem vazios, apenas os ativos cujos subtipos estão em <span class="codeph"> assetSubTypeArray</span> serão devolvidos. </p> <p>Se <span class="codeph"> false</span>, ativos sem subtipo definido serão incluídos. </p> <p>O valor padrão é <span class="codeph"> false</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Contém uma lista de campos e subcampos incluídos na resposta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:StringArray</span> </td> 
   <td colname="col3"> Não </td> 
   <td colname="col4"> Contém uma lista de campos e subcampos excluídos da resposta. </td> 
  </tr> 
 </tbody> 
</table>

**Saída (getAssetsByNameReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`assetArray`*` | `types:AssetArray` | Não | Matriz de ativos que correspondem aos critérios de filtragem. |

## Exemplos {#section-3b7447398e574c88aeaf8ca159cc78dd}

Essa amostra de código retorna dois ativos de tipo de imagem.

**Solicitação**

```java
<getAssetsByNameParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <nameArray>
      <items>B010</items>
      <items>IMG_0103</items>
   </nameArray>
   <assetTypeArray>
      <items>Image</items>
   </assetTypeArray>
</getAssetsByNameParam>
```

**Resposta**

```java
<getAssetsByNameReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <assetArray>
      <items>
         <assetHandle>a|210</assetHandle>
         <type>Image</type>
         <name>B010</name>
         ...</items>
      <items>
         <assetHandle>a|189</assetHandle>
         <type>Image</type>
         <name>IMG_0103</name>
         ...
      </items>
   </assetArray>
</getAssetsByNameReturn>
```

