---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 48be47f6-4c1c-4f19-afa7-f643e504c287
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '30'
ht-degree: 13%

---

# ipsApiFault{#ipsapifault}

Sintaxe

## Tipos de falhas {#section-425697675cac4b2ab5c48bd463956401}

| ID | Falha |
|---|---|
| 30000 | `IPS_API_FAULT_CODE_EXCEPTION` |
| 30001 | `IPS_API_FAULT_CODE_INVALID_PARAMETER` |
| 30002 | `IPS_API_FAULT_CODE_MISSING_PARAMETER` |
| 30003 | `IPS_API_FAULT_CODE_INVALID_REQUEST_XML` |

## Campos de falha {#section-37fe1aef1d5f4ca480071ca933aba826}

| Nome | Tipo | Descrição |
|---|---|---|
| `code` | `xsd:int` | ID de falha |
| `reason` | `xsd:string` | Uma mensagem informativa descrevendo a falha. |
