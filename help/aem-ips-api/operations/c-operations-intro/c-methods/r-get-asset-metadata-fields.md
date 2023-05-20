---
description: Retorna todos os campos de metadados, agrupados por tipo de ativo.
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 5234d3ea-c333-4e35-91ae-ce3412919fda
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 0%

---

# getAssetMetadataFields{#getassetmetadatafields}

Retorna todos os campos de metadados, agrupados por tipo de ativo.

Sintaxe

## Tipos de usuário autorizados {#section-e19a9d21cc2b45469c233d4ae55ebfc2}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-5dd58970d61d4d4a928e36ffceca6f5e}

**Entrada (getAssetMetadataFieldsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa cujos metadados você deseja recuperar. |

**Saída (getAssetMetadataFieldsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| assetFieldArray | `types:AssetMetadataFieldsArray` | Sim | Matriz de campos de metadados, por tipo de ativo. |

## Exemplos {#section-d79ab85f29144635b0b61416e52f4f3f}

**Solicitação**

```java
<getAssetMetadataFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
</getAssetMetadataFieldsParam>
```

**Resposta**

>[!NOTE]
>
>Truncado por brevidade.

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```
