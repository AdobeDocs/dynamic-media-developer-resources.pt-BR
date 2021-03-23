---
description: Um usuário de recursos e tipos no sistema.
seo-description: Um usuário de recursos e tipos no sistema.
seo-title: Usuário
solution: Experience Manager
title: Usuário
uuid: 37e939ae-dd1a-4550-aa93-b7b091ebc339
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
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

