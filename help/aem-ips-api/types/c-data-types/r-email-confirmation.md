---
description: Envia um email para um recipient designado em resposta a uma operação cdnCacheInvalidation.
solution: Experience Manager
title: ConfirmaçãoDeEmail
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---


# EmailConfirmation{#emailconfirmation}

Envia um email para um recipient designado em resposta a uma operação cdnCacheInvalidation.

Sintaxe

## Parâmetros {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | Se verdadeiro, inclui a conta de usuário do serviço da Web do usuário, que é uma lista de emails designados para receber uma confirmação por email da CDN da Dynamic Media. |
| `*`ccOtherArray`*` | `types:EmailArray` | Uma matriz de endereços de email (no máximo 5) designados para receber a notificação de confirmação da CDN da Dynamic Media. |

