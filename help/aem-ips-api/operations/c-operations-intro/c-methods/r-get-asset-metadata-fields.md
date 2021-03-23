---
description: Retorna todos os campos de metadados, agrupados por tipo de ativo.
seo-description: Retorna todos os campos de metadados, agrupados por tipo de ativo.
seo-title: getAssetMetadataFields
solution: Experience Manager
title: getAssetMetadataFields
uuid: 01d5076f-f187-4069-b2f2-806fb1d8be84
feature: Dynamic Media Classic, SDK/API, metadados, gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
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
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa cujos metadados você deseja recuperar. |

**Saída (getAssetMetadataFieldsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`assetFieldArray`*` | `types:AssetMetadataFieldsArray` | Sim | Matriz de campos de metadados, por tipo de ativo. |

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
>Truncado para brevidade.

```java
<getAssetMetadataFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <assetFieldsArray>
      <items>
         <assetType>Asset</assetType>
     </items>
   </assetFieldsArray>
<getAssetMetadataFieldsReturn>
```

