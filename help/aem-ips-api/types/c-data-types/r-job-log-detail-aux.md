---
description: Contém mensagens suplementares associadas à mensagem de registro de tarefas principal (JobDetail). Inclui avisos e outros detalhes associados ao ativo processado no momento.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---

# JobLogDetailAux{#joblogdetailaux}

Contém mensagens suplementares associadas à mensagem de registro de tarefas principal (JobDetail). Inclui avisos e outros detalhes associados ao ativo processado no momento.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| logMessage | `xsd:string` | Uma mensagem auxiliar. |
| logType | `xsd:string` | Tipo de log: `IPSJobLog.gcUploadWarning` ou `IPSJobLog.gcUploadError`. |
| dateCreated | `xsd:dateTime` | Data de criação do log de trabalho auxiliar. |
