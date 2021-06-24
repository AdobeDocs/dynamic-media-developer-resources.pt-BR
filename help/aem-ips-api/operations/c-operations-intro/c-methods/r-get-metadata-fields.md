---
description: Obtém os campos de metadados definidos pelo usuário associados a um ativo.
solution: Experience Manager
title: getMetadataFields
feature: Dynamic Media Classic, SDK/API, Metadados
role: Developer,Administrator
exl-id: 4d01e2e7-9b68-4dfa-9fe8-08a22cb4bfd5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
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
