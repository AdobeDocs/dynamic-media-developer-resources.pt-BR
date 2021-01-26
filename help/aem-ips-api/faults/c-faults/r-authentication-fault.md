---
description: Acionado quando um usuário não pode ser autenticado.
solution: Experience Manager
title: authenticationFault
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 8%

---


# authenticationFault{#authenticationfault}

Acionado quando um usuário não pode ser autenticado.

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
