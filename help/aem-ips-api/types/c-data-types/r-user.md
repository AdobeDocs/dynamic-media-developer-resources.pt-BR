---
description: Um usuário de recursos e tipos no sistema.
solution: Experience Manager
title: Usuário
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# Usuário{#user}

Um usuário de recursos e tipos no sistema.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`userHandle`*` | `xsd:string` | Identificador do usuário. |
| `*`firstName`*` | `xsd:string` | Nome do usuário. |
| `*`lastName`*` | `xsd:string` | Sobrenome do usuário. |
| `*`email`*` | `xsd:string` | endereço de email. |
| `*`defaultRole`*` | `xsd:string` | Define a função de um usuário em cada empresa à qual ele pertence. No entanto, a função de usuário `IpsAmin` substitui outras funções de usuário. |
| `*`isValid`*` | `xsd:boolean` | Determina se o usuário é válido. |
| `*`passwordExpires`*` | `xsd:dateTime` | Define a data de expiração da senha. |
