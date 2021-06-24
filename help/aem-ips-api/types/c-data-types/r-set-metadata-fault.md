---
description: Detalhes de aviso ou erro para uma atualização de uso em uma operação batchSetAssetMetadata.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic, SDK/API, Metadados
role: Developer,Administrator
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# SetMetadataFault{#setmetadatafault}

Detalhes de aviso ou erro para uma atualização de uso em uma operação batchSetAssetMetadata.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | O ativo cujos metadados foram definidos sem êxito. |
| `*`fieldHandle`*` | `xsd:string` | O identificador do campo de metadados cujo valor foi definido sem êxito. |
| `*`código`*` | `xsd:int` | Código de falha. |
| `*`reason`*` | `xsd:string` | Descrição de falha (texto simples). |
