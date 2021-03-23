---
description: Obtém um tipo de conjunto de propriedades usando um identificador para uma empresa e o nome do tipo de conjunto de propriedades. Ele obtém uma estrutura do tipo com o identificador para o tipo , bem como o tipo de propriedade.
seo-description: Obtém um tipo de conjunto de propriedades usando um identificador para uma empresa e o nome do tipo de conjunto de propriedades. Ele obtém uma estrutura do tipo com o identificador para o tipo , bem como o tipo de propriedade.
seo-title: getPropertySetType
solution: Experience Manager
title: getPropertySetType
uuid: 203fa949-a81e-455a-a83e-576b6f65e3af
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# getPropertySetType{#getpropertysettype}

Obtém um tipo de conjunto de propriedades usando um identificador para uma empresa e o nome do tipo de conjunto de propriedades. Ele obtém uma estrutura do tipo com o identificador para o tipo , bem como o tipo de propriedade.

Sintaxe

## Tipos de usuário autorizados {#section-2b291d32f95b4a3d854429124cbae24c}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-c9a53400c44744668bd7915f72d2bf3d}

**Entrada (getPropertySetTypeParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Não | O nome da empresa. Opcional, pois um tipo de conjunto de propriedades pode pertencer a várias empresas. |
| `*`name`*` | `xsd:string` | Sim | Nome do tipo de conjunto de propriedades. |

**Saída (getPropertySetTypeReturn)**

<table id="table_F2724F6B706C4F658AED99290E29F3E6"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> type</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipos:PropertySetType</span> </td> 
   <td colname="col3"> Sim </td> 
   <td colname="col4">A estrutura de tipo que contém um: 
    <ul id="ul_FC028882124D4CD6870A076CBFB80333"> 
     <li id="li_9F36539C51ED48EDBECCD6A07A4FDD4A">Manipule. </li> 
     <li id="li_6004406A0D1341648A714FF3C61E4004">Digite o nome. </li> 
     <li id="li_29F6CA9D8B134ED3B10B6BDBB41BF607">Tipo de propriedade. </li> 
     <li id="li_A2354354541A4F1AB7234F65F2B61A40">Valor que indica se o tipo permite vários tipos de propriedade. </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

## Exemplos {#section-1b57199415e34a8fa449f864f8895b14}

Essa amostra de código retorna um tipo de conjunto de propriedades por nome.

**Solicitação**

```java
<getPropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <name>Adobe.UserProperty</name>
</getPropertySetTypeParam>
```

**Resposta**

```java
<getPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <type>
      <typeHandle>pt|10801</typeHandle>
      <name>Adobe.UserProperty</name>
      <propertyType>UserProperty</propertyType>
      <allowMultiple>false</allowMultiple></type>
</getPropertySetTypeReturn>
```

