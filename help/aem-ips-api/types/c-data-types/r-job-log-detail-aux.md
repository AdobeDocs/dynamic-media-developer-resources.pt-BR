---
description: Contém mensagens suplementares associadas à mensagem de registro de tarefas principal (JobDetail). Inclui avisos e outros detalhes associados ao ativo processado no momento.
seo-description: Contém mensagens suplementares associadas à mensagem de registro de tarefas principal (JobDetail). Inclui avisos e outros detalhes associados ao ativo processado no momento.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# JobLogDetailAux{#joblogdetailaux}

Contém mensagens suplementares associadas à mensagem de registro de tarefas principal (JobDetail). Inclui avisos e outros detalhes associados ao ativo processado no momento.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Uma mensagem auxiliar. |
| `*`logType`*` | `xsd:string` | Tipo de log: `IPSJobLog.gcUploadWarning` ou `IPSJobLog.gcUploadError`. |
| `*`dateCreated`*` | `xsd:dateTime` | Data de criação do log de trabalho auxiliar. |

