---
description: Lançado quando um usuário não pode ser autenticado.
solution: Experience Manager
title: authenticationFault
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: fce5c227-9291-4d17-801f-4ef4b8d43eb4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '42'
ht-degree: 7%

---

# authenticationFault{#authenticationfault}

Lançado quando um usuário não pode ser autenticado.

Sintaxe

## Tipos de falhas {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | Falha |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## Campos de falha {#section-1fe84846a7154b03ab49552810ee9ac3}

| Nome | Tipo | Descrição |
|---|---|---|
| `code` | `xsd:int` | ID de falha |
| `reason` | `xsd:string` | Uma mensagem informativa descrevendo a falha. |
