---
description: Contém mensagens suplementares associadas à mensagem principal do log de trabalhos (JobDetail). Inclui avisos e outros detalhes associados ao ativo processado no momento.
seo-description: Contém mensagens suplementares associadas à mensagem principal do log de trabalhos (JobDetail). Inclui avisos e outros detalhes associados ao ativo processado no momento.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
topic: Scene7 Image Production System API
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JobLogDetailAux{#joblogdetailaux}

Contém mensagens suplementares associadas à mensagem principal do log de trabalhos (JobDetail). Inclui avisos e outros detalhes associados ao ativo processado no momento.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| ` *`logMessage`*` | `xsd:string` | Uma mensagem auxiliar. |
| ` *`logType`*` | `xsd:string` | Tipo de registro: `IPSJobLog.gcUploadWarning` ou `IPSJobLog.gcUploadError`. |
| ` *`dateCreated`*` | `xsd:dateTime` | Data de criação do log de trabalho auxiliar. |

