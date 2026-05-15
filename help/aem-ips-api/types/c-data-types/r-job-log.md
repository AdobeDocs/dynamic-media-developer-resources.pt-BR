---
description: O log de tarefas após a execução da tarefa.
solution: Experience Manager
title: JobLog
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80ae6669-6fe7-45a6-9a1d-f8544dd4f878
TQID: 'https://experienceleague.adobe.com/R3h5NRNxH00Qskdzvw6ul55STF234SudJbjLGYrd238'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 187
ht-degree: 0%

---

# [!DNL JobLog]{#joblog}

O log de tarefas após a execução da tarefa.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| companyHandle | `xsd:string` | Identificador da empresa. |
| jobHandle | `xsd:string` | Identificador do trabalho. |
| jobName | `xsd:string` | Nome do trabalho. |
| originalJobName | `xsd:string` | O nome original enviado para o trabalho com `submitJob`. |
| submitUserEmail | `xsd:string` | O endereço de email do usuário que enviou o trabalho. |
| logType | `xsd:string` | Escolha de tipos de log de job. |
| jobSubType | `xsd:string` | Informações adicionais sobre o cargo. |
| startDate | `xsd:dateTime` | A data inicial, a hora e o fuso horário do trabalho. |
| endDate | `xsd:dateTime` | A data, hora e fuso horário de término do trabalho. |
| [!DNL description] | `xsd:string` | Uma descrição do trabalho conforme originalmente especificado em `submitJob`. |
| fileSuccessCount | `xsd:int` | Número de arquivos processados com êxito. |
| fileErrorCount | `xsd:int` | Número de arquivos que causaram um erro. |
| fileWarningCount | `xsd:int` | Número de arquivos que geraram um aviso. |
| fileDuplicateCount | `xsd:int` | Número de arquivos duplicados. |
| fileUpdateCount | `xsd:int` | Número de arquivos atualizados. |
| totalFileCount | `xsd:int` | Número de arquivos processados pelo trabalho registrado. |
| transferSuccessCount | `xsd:int` | Número de transferências bem-sucedidas. |
| transferErrorCount | `xsd:int` | Número de erros de transferência. |
| transferWarningCount | `xsd:int` | Número de avisos de transferência. |
| fatalError | `xsd:boolean` | Se o trabalho gerou um erro fatal. |
| detailTotalRows | `xsd:int` | O número total de linhas correspondentes à consulta, que pode ser maior do que o tamanho de `detailArray` devido a limites de tamanho de página. |
| detailArray | `types:JobLogDetailArray` | A matriz de detalhes sobre o trabalho registrado. |
