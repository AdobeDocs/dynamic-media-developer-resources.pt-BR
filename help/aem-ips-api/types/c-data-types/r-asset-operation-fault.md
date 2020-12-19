---
description: Contém informações sobre condições de aviso ou erro geradas durante uma operação de ativo em lote. Os campos de código e motivo correspondem aos campos de mensagem de falha que teriam sido lançados para a operação equivalente não em lote.
seo-description: Contém informações sobre condições de aviso ou erro geradas durante uma operação de ativo em lote. Os campos de código e motivo correspondem aos campos de mensagem de falha que teriam sido lançados para a operação equivalente não em lote.
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
topic: Scene7 Image Production System API
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# AssetOperationFault{#assetoperationfault}

Contém informações sobre condições de aviso ou erro geradas durante uma operação de ativo em lote. Os campos de código e motivo correspondem aos campos de mensagem de falha que teriam sido lançados para a operação equivalente não em lote.

Sintaxe

## Parâmetros {#section-c906f052f43e4785ba46d92b514b0923}

| Nome | Tipo | Descrição |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Identificador de ativos para a operação com falha. |
| ` *`código`*` | `xsd:int` | Código de falha da operação. |
| ` *`razão`*` | `xsd:string` | Descrição ou motivo de falha. |

