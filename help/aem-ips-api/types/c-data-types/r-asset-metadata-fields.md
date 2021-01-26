---
description: Retorna definições de campos de metadados para tipos de ativos especificados.
seo-description: Retorna definições de campos de metadados para tipos de ativos especificados.
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
topic: Dynamic Media Image Production System API
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---


# AssetMetadataFields{#assetmetadatafields}

Retorna definições de campos de metadados para tipos de ativos especificados.

Sintaxe

## Parâmetros {#section-5ad771540c5f40c187b35e34aac19305}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Tipo de ativo associado às definições de campo (consulte &quot;Tipos de ativo&quot; para obter valores). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Matriz de definições de campos de metadados associadas ao tipo de ativo especificado em `assetType`. |

