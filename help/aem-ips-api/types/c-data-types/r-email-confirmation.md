---
description: Envia um email para um recipient designado em resposta a uma operação cdnCacheInvalidation.
solution: Experience Manager
title: ConfirmaçãoDeEmail
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 0%

---


# Confirmação de Email{#emailconfirmation}

Envia um email para um recipient designado em resposta a uma operação cdnCacheInvalidation.

Sintaxe

## Parâmetros {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | Se true, inclui a conta de usuário do serviço da Web do usuário, que é uma lista de emails designados para receber uma confirmação por email do Dynamic Media CDN. |
| `*`ccOthersArray`*` | `types:EmailArray` | Uma matriz de endereços de email (no máximo 5) designada para receber a notificação de confirmação do Dynamic Media CDN. |

