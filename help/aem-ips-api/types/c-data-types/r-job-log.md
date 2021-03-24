---
description: O log de tarefas após a execução da tarefa.
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---


# JobLog{#joblog}

O log de tarefas após a execução da tarefa.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Manuseio da empresa. |
| `*`jobHandle`*` | `xsd:string` | Identificador da tarefa. |
| `*`jobName`*` | `xsd:string` | Nome da tarefa. |
| `*`originalJobName`*` | `xsd:string` | O nome original enviado para o trabalho com `submitJob`. |
| `*`submitUserEmail`*` | `xsd:string` | O endereço de email do usuário que enviou o trabalho. |
| `*`logType`*` | `xsd:string` | Escolha dos tipos de log de trabalho. |
| `*`jobSubType`*` | `xsd:string` | Informações adicionais sobre o trabalho. |
| `*`startDate`*` | `xsd:dateTime` | A data de início, a hora e o fuso horário da tarefa. |
| `*`endDate`*` | `xsd:dateTime` | A data final, a hora e o fuso horário da tarefa. |
| `*`descrição`*` | `xsd:string` | Uma descrição da tarefa conforme especificado originalmente em `submitJob`. |
| `*`fileSuccessCount`*` | `xsd:int` | Número de arquivos processados com êxito. |
| `*`fileErrorCount`*` | `xsd:int` | Número de arquivos que causaram um erro. |
| `*`fileWarningCount`*` | `xsd:int` | Número de arquivos que geraram um aviso. |
| `*`fileDuplicateCount`*` | `xsd:int` | Número de arquivos duplicados. |
| `*`fileUpdateCount`*` | `xsd:int` | Número de arquivos atualizados. |
| `*`totalFileCount`*` | `xsd:int` | Número de arquivos processados pelo trabalho registrado. |
| `*`transferSuccessCount`*` | `xsd:int` | Número de transferências bem-sucedidas. |
| `*`transferErrorCount`*` | `xsd:int` | Número de erros de transferência. |
| `*`transferWarningCount`*` | `xsd:int` | Número de avisos de transferência. |
| `*`fatalError`*` | `xsd:boolean` | Se o trabalho gerou um erro fatal. |
| `*`detailTotalRows`*` | `xsd:int` | O número total de linhas correspondentes ao query, que pode ser maior que o tamanho de `detailArray` devido aos limites de tamanho da página. |
| `*`detailArray`*` | `types:JobLogDetailArray` | A matriz de detalhes sobre o trabalho registrado. |

