---
description: Retorna definições de campo de metadados para tipos de ativos especificados.
seo-description: Retorna definições de campo de metadados para tipos de ativos especificados.
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
feature: Dynamic Media Classic, SDK/API, metadados, gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
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

