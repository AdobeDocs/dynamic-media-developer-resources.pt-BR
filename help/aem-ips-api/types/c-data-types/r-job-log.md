---
description: O log de tarefas após a execução do trabalho.
seo-description: O log de tarefas após a execução do trabalho.
seo-title: JobLog
solution: Experience Manager
title: JobLog
topic: Dynamic Media Image Production System API
uuid: d267009a-e4ad-4a21-ae0e-caf51d2f338b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 0%

---


# JobLog{#joblog}

O log de tarefas após a execução do trabalho.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Alça da empresa. |
| `*`jobHandle`*` | `xsd:string` | Trabalho. |
| `*`jobName`*` | `xsd:string` | Nome do trabalho. |
| `*`originalJobName`*` | `xsd:string` | O nome original enviado para o trabalho com `submitJob`. |
| `*`submitUserEmail`*` | `xsd:string` | O endereço de email do usuário que enviou o serviço. |
| `*`logType`*` | `xsd:string` | Escolha dos tipos de log de trabalhos. |
| `*`jobSubType`*` | `xsd:string` | Informações adicionais sobre o cargo. |
| `*`startDate`*` | `xsd:dateTime` | A data, a hora e o fuso horário do start do serviço. |
| `*`endDate`*` | `xsd:dateTime` | A data final, a hora e o fuso horário do trabalho. |
| `*`descrição`*` | `xsd:string` | Uma descrição do trabalho conforme especificado originalmente em `submitJob`. |
| `*`fileSuccessCount`*` | `xsd:int` | Número de arquivos processados com êxito. |
| `*`fileErrorCount`*` | `xsd:int` | Número de arquivos que causaram um erro. |
| `*`fileWarningCount`*` | `xsd:int` | Número de arquivos que geraram um aviso. |
| `*`fileDuplicateCount`*` | `xsd:int` | Número de arquivos de duplicado. |
| `*`fileUpdateCount`*` | `xsd:int` | Número de arquivos atualizados. |
| `*`totalFileCount`*` | `xsd:int` | Número de arquivos processados pelo trabalho registrado. |
| `*`transferSuccessCount`*` | `xsd:int` | Número de transferências bem-sucedidas. |
| `*`transferErrorCount`*` | `xsd:int` | Número de erros de transferência. |
| `*`transferWarningCount`*` | `xsd:int` | Número de avisos de transferência. |
| `*`fatalError`*` | `xsd:boolean` | Se o trabalho gerou um erro fatal. |
| `*`detailTotalRows`*` | `xsd:int` | O número total de linhas correspondentes ao query, que pode ser maior que o tamanho de `detailArray` devido aos limites de tamanho da página. |
| `*`detailArray`*` | `types:JobLogDetailArray` | A matriz de detalhes sobre o trabalho registrado. |

