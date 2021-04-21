---
description: Retorna definições de campo de metadados para tipos de ativos especificados.
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 0%

---


# AssetMetadataFields{#assetmetadatafields}

Retorna definições de campo de metadados para tipos de ativos especificados.

Sintaxe

## Parâmetros {#section-5ad771540c5f40c187b35e34aac19305}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Tipo de ativo associado às definições de campo (consulte &quot;Tipos de ativo&quot; para obter valores). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Matriz de definições de campos de metadados associadas ao tipo de ativo especificado em `assetType`. |

