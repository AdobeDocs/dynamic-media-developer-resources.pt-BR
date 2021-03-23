---
description: Obtém os campos de metadados definidos pelo usuário associados a um ativo.
seo-description: Obtém os campos de metadados definidos pelo usuário associados a um ativo.
seo-title: getMetadataFields
solution: Experience Manager
title: getMetadataFields
uuid: bf891bae-53c8-4e3d-90df-caca9a7e022b
feature: Dynamic Media Classic, SDK/API, Metadados
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# getMetadataFields{#getmetadatafields}

Obtém os campos de metadados definidos pelo usuário associados a um ativo.

Sintaxe

## Tipos de usuário autorizados {#section-e32e481a02674b729bfc5454a6c9ff65}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-bac949e59c0546429c5786fe422d750d}

**Entrada (getMetadataFieldsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O responsável da empresa. |
| `*`assetType`*` | `xsd:string` | Sim | Tipos de ativos a partir dos quais obter metadados. |

**Saída (getMetadataFieldsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`Frase do código`*` | `Code Phrase` |  |  |

## Exemplos {#section-dbfde1483d614b5aac2b491cb32115d7}

Essa amostra de código retorna ativos de metadados para o tipo e empresa especificados. A resposta contém uma matriz de campos de metadados em uma matriz de campos. Nem todos os ativos têm os mesmos metadados. O usuário IPS define o campo de metadados do ativo.

**Solicitação**

```java
<ns1:getMetadataFieldsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetType>Pdf</ns1:assetType>
</ns1:getMetadataFieldsParam>
```

**Resposta**

```java
<getMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <fieldArray>
      <items>
         <fieldHandle>47|ALL|Resolution</fieldHandle>
         <name>Resolution</name>
         <type>String</type>
         <defaultValue>120</defaultValue>
         <isRequired>false</isRequired>
         <isUserDefined>true</isUserDefined>
      </items>
   </fieldArray>
</getMetadataFieldsReturn>
```

