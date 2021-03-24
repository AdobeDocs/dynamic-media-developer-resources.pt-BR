---
description: Detalhes de aviso ou erro para uma atualização de uso em uma operação batchSetAssetMetadata.
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic, SDK/API, Metadados
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '66'
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

