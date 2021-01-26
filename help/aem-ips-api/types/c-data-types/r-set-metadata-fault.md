---
description: Detalhes de aviso ou erro para uma atualização de uso em uma operação batchSetAssetMetadata.
seo-description: Detalhes de aviso ou erro para uma atualização de uso em uma operação batchSetAssetMetadata.
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
topic: Dynamic Media Image Production System API
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '71'
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
| `*`razão`*` | `xsd:string` | Descrição de falha (texto simples). |

