---
description: Envia um email para um recipient designado em resposta a uma operação cdnCacheInvalidation.
solution: Experience Manager
title: ConfirmaçãoDeEmail
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# ConfirmaçãoDeEmail{#emailconfirmation}

Envia um email para um recipient designado em resposta a uma operação cdnCacheInvalidation.

Sintaxe

## Parâmetros {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | Se true, inclui a conta de usuário do serviço da Web do usuário, que é uma lista de emails designados para receber uma confirmação por email do Dynamic Media CDN. |
| `*`ccOthersArray`*` | `types:EmailArray` | Uma matriz de endereços de email (no máximo 5) designada para receber a notificação de confirmação do Dynamic Media CDN. |
