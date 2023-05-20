---
description: Detalhes de aviso ou erro para uma atualização de uso em uma operação batchSetAssetMetadata.
solution: Experience Manager
title: DefinirFalhaDeMetadados
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 0%

---

# [!DNL SetMetadataFault]{#setmetadatafault}

Detalhes de aviso ou erro para uma atualização de uso em uma operação batchSetAssetMetadata.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| assetHandle | `xsd:string` | O ativo cujos metadados foram definidos sem sucesso. |
| fieldHandle | `xsd:string` | O identificador do campo de metadados cujo valor foi definido sem sucesso. |
| código | `xsd:int` | Código de falha. |
| motivo | `xsd:string` | Descrição da falha (texto simples). |
