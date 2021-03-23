---
description: Contém informações sobre condições de aviso ou erro geradas durante uma operação de ativo em lote. Os campos de código e motivo correspondem aos campos de mensagem de falha que teriam sido lançados para a operação equivalente não em lote.
seo-description: Contém informações sobre condições de aviso ou erro geradas durante uma operação de ativo em lote. Os campos de código e motivo correspondem aos campos de mensagem de falha que teriam sido lançados para a operação equivalente não em lote.
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# AssetOperationFault{#assetoperationfault}

Contém informações sobre condições de aviso ou erro geradas durante uma operação de ativo em lote. Os campos de código e motivo correspondem aos campos de mensagem de falha que teriam sido lançados para a operação equivalente não em lote.

Sintaxe

## Parâmetros {#section-c906f052f43e4785ba46d92b514b0923}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Identificador de ativo para a operação com falha. |
| `*`código`*` | `xsd:int` | Código de falha da operação. |
| `*`reason`*` | `xsd:string` | Descrição ou motivo da falha. |

