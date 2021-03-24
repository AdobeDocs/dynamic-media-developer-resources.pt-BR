---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '32'
ht-degree: 12%

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

