---
description: Informações do registro de tarefas.
seo-description: Informações do registro de tarefas.
seo-title: JobLogDetail
solution: Experience Manager
title: JobLogDetail
topic: Dynamic Media Image Production System API
uuid: cb1879d7-a554-4ff0-bba0-0758c43f2a99
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---


# JobLogDetail{#joblogdetail}

Informações do registro de tarefas.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Mensagens no registro de tarefas. |
| `*`logType`*` | `xsd:string` | Tipo de arquivo de log de trabalho. |
| `*`assetName`*` | `xsd:string` | Nome do ativo no registro de tarefas (opcional). |
| `*`assetType`*` | `xsd:string` | Escolha do tipo de ativo. |
| `*`assetHandle`*` | `xsd:string` | Identificador de ativos referenciado no registro de tarefas. |
| `*`auxArray`*` | `types:JobLogDetailAuxArray` | Fornece informações adicionais detalhadas sobre o log de trabalhos além dos cinco tipos de log de trabalhos descritos acima. |

