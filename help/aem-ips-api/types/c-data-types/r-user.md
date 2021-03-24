---
description: Um usuário de recursos e tipos no sistema.
solution: Experience Manager
title: Usuário
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
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

