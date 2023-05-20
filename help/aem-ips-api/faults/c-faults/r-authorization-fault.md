---
description: Lançado quando um usuário autenticado tem permissões insuficientes para realizar uma tarefa.
solution: Experience Manager
title: authorizationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 76965735-92d8-46be-b589-67cad3b987dc
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 18%

---

# authorizationFault{#authorizationfault}

Lançado quando um usuário autenticado tem permissões insuficientes para realizar uma tarefa.

Sintaxe

## Tipos de falhas {#section-1f04dec489714ee6bb7256fae6ab7730}

| ID | Falha |
|---|---|
| 20000 | `AUTHORIZATION_FAULT_CODE_INVALID_COMPANY` |
| 20001 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USERNAME` |
| 20002 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USER` |
| 20003 | `AUTHORIZATION_FAULT_CODE_NO_OPERATION_PERMISSION` |
| 20004 | `AUTHORIZATION_FAULT_CODE_NO_IMPERSONATION_PERMISSION` |
| 20005 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_PARAMETER_VALUE` |
| 20006 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_COMPANY` |
| 20007 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_REQUEST_USER` |
| 20008 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_ACCESS_GROUP` |
| 20009 | `AUTHORIZATION_FAULT_CODE_MISSING_PERMISSION` |

## Campos de falha {#section-4e3e41f41fea402a9ae314bfd05f663e}

| Nome | Tipo | Descrição |
|---|---|---|
| `code` | `xsd:int` | ID da falha |
| `reason` | `xsd:string` | Uma mensagem informativa descrevendo a falha. |
