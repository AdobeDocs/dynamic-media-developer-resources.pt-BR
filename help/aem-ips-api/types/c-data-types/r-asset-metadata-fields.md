---
description: Retorna definições de campo de metadados para tipos de ativos especificados.
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic, SDK/API, metadados, gerenciamento de ativos
role: Developer,Administrator
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '56'
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
