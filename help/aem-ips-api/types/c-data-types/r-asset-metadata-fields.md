---
title: AssetMetadataFields
description: Retorna definições de campo de metadados para tipos de ativos especificados.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '48'
ht-degree: 0%

---

# AssetMetadataFields{#assetmetadatafields}

Retorna definições de campo de metadados para tipos de ativos especificados.

Sintaxe

## Parâmetros {#section-5ad771540c5f40c187b35e34aac19305}

| Nome | Tipo | Descrição |
|---|---|---|
| assetType | `xsd:string` | Tipo de ativo associado às definições de campo (consulte &quot;Tipos de ativo&quot; para obter valores). |
| fieldArray | `types:MetadataFieldArray` | Matriz de definições de campos de metadados associadas ao tipo de ativo especificado em `assetType`. |
