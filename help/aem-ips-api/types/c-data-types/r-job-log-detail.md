---
description: Informações do log de trabalhos.
seo-description: Informações do log de trabalhos.
seo-title: JobLogDetail
solution: Experience Manager
title: JobLogDetail
uuid: cb1879d7-a554-4ff0-bba0-0758c43f2a99
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---


# JobLogDetail{#joblogdetail}

Informações do log de trabalhos.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Mensagens no log de tarefas. |
| `*`logType`*` | `xsd:string` | Tipo de arquivo de log da tarefa. |
| `*`assetName`*` | `xsd:string` | Nome do ativo no log de trabalho (opcional). |
| `*`assetType`*` | `xsd:string` | Escolha do tipo de ativo. |
| `*`assetHandle`*` | `xsd:string` | Identificador de ativo referenciado no log de trabalho. |
| `*`auxArray`*` | `types:JobLogDetailAuxArray` | Fornece informações adicionais detalhadas sobre o log de trabalhos além dos cinco tipos de log de trabalhos descritos acima. |

