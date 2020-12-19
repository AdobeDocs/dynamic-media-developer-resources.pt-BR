---
description: Envia um email para um recipient designado em resposta a uma operação cdnCacheInvalidation.
seo-description: Envia um email para um recipient designado em resposta a uma operação cdnCacheInvalidation.
seo-title: ConfirmaçãoDeEmail
solution: Experience Manager
title: ConfirmaçãoDeEmail
topic: Scene7 Image Production System API
uuid: c3b7aada-a03a-418d-80b2-31a86a1af786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---


# EmailConfirmation{#emailconfirmation}

Envia um email para um recipient designado em resposta a uma operação cdnCacheInvalidation.

Sintaxe

## Parâmetros {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nome | Tipo | Descrição |
|---|---|---|
| ` *`ccOriginator`*` | `xsd:boolean` | Se verdadeiro, inclui a conta de usuário do serviço da Web do usuário, que é uma lista de emails designados para receber uma confirmação por email da CDN da Scene7. |
| ` *`ccOtherArray`*` | `types:EmailArray` | Uma matriz de endereços de email (no máximo 5) designados para receber a notificação de confirmação da CDN da Scene7. |

