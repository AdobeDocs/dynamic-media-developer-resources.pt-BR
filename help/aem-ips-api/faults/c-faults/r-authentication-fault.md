---
description: Lançado quando um usuário não pode ser autenticado.
solution: Experience Manager
title: authenticationFault
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 6%

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
