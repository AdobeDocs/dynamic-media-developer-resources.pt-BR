---
title: AssetOperationFault
description: Contém informações sobre condições de aviso ou erro geradas durante uma operação de ativo em lote. Os campos de código e motivo correspondem aos campos de mensagem de falha que teriam sido lançados para a operação equivalente não em lote.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# [!DNL AssetOperationFault]{#assetoperationfault}

Contém informações sobre condições de aviso ou erro geradas durante uma operação de ativo em lote. Os campos de código e motivo correspondem aos campos de mensagem de falha que teriam sido lançados para a operação equivalente não em lote.

Sintaxe

## Parâmetros {#section-c906f052f43e4785ba46d92b514b0923}

| Nome | Tipo | Descrição |
|---|---|---|
| assetHandle | `xsd:string` | Identificador de ativo para a operação com falha. |
| código | `xsd:int` | Código de falha da operação. |
| reason | `xsd:string` | Descrição ou motivo da falha. |
