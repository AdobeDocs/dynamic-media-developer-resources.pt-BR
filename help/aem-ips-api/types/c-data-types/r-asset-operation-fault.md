---
description: Contém informações sobre condições de aviso ou erro geradas durante uma operação de ativo em lote. Os campos de código e motivo correspondem aos campos de mensagem de falha que teriam sido lançados para a operação equivalente não em lote.
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Developer,Administrator
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
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
