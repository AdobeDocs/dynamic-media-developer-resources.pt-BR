---
description: Gerencia direitos de acesso, modificação, criação ou exclusão de ativos por grupo.
solution: Experience Manager
title: Permissão
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '53'
ht-degree: 0%

---

# [!DNL Permission]{#permission}

Gerencia direitos de acesso, modificação, criação ou exclusão de ativos por grupo.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| groupHandle | `xsd:string` | Identificador de grupo. |
| groupName | `xsd:string` | Nome do grupo. |
| permissionType | `xsd:string` | Escolha do tipo de permissão. |
| isAllowed | `xsd:boolean` | Determina se a permissão é permitida. |
| isOverride | `xsd:boolean` | Determina se a permissão substitui outra. |
