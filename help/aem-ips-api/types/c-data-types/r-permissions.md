---
description: Gerencia direitos para acessar, modificar, criar ou excluir ativos por grupo.
solution: Experience Manager
title: Permissão
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 18e5f8f6-3cbe-4d36-b02a-5a3002e4498c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '54'
ht-degree: 0%

---

# Permissão{#permission}

Gerencia direitos para acessar, modificar, criar ou excluir ativos por grupo.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| groupHandle | `xsd:string` | Identificador de grupo. |
| groupName | `xsd:string` | Nome do grupo. |
| permissionType | `xsd:string` | Escolha do tipo de permissão. |
| isAllowed | `xsd:boolean` | Determina se a permissão é permitida. |
| isOverride | `xsd:boolean` | Determina se a permissão substitui outra. |
