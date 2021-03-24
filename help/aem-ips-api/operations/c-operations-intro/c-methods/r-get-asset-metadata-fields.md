---
description: Retorna todos os campos de metadados, agrupados por tipo de ativo.
solution: Experience Manager
title: getAssetMetadataFields
feature: Dynamic Media Classic, SDK/API, metadados, gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '73'
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

