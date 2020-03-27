---
description: Acionado quando um usuário não pode ser autenticado.
seo-description: Acionado quando um usuário não pode ser autenticado.
seo-title: authenticationFault
solution: Experience Manager
title: authenticationFault
topic: Scene7 Image Production System API
uuid: 89cc6f09-def6-4db1-a8b5-410909693dce
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# authenticationFault{#authenticationfault}

Acionado quando um usuário não pode ser autenticado.

Sintaxe

## Tipos de falha {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

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

