---
description: Obtém logs de trabalho especificados para a empresa selecionada. Você pode classificar por caracteres, direção, datas de início e término e número de linhas.
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 0%

---

# getJobLogs{#getjoblogs}

Obtém logs de trabalho especificados para a empresa selecionada. Você pode classificar por caracteres, direção, datas de início e término e número de linhas.

Sintaxe

## Tipos de usuário autorizados {#section-9df82972265d44c9ad91504a17c3ffa6}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-8cfdc7994da24678a45edcb37e9a2166}

**Entrada (getJobLogsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Não | O identificador da empresa. |
| userHandle | `xsd:string` | Não | Obtém logs de trabalhos enviados por um usuário específico. |
| sortBy | `xsd:string` | Não | Permite selecionar campos de classificação. |
| sortDirection | `xsd:string` | Não | Ordem de classificação (crescente ou decrescente). |
| startDate | `xsd:dateTime` | Não | A data e a hora de início do log de trabalho. Forneça o fuso horário com a solicitação para esse campo. |
| endDate | `xsd:dateTime` | Não | A data e a hora de término do log de trabalho. Forneça o fuso horário com a solicitação para esse campo. |
| numRows | `xsd:int` | Não | Número máximo de linhas a retornar. |

**Saída (getJobLogsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| jobLogArray | `types: JobLogArray` | Sim | Matriz de logs de trabalho. |

## Exemplos {#section-35871c94b4a44559912577efddbc46a6}

Esta amostra de código retorna logs de trabalho de IPS para uma empresa específica. Você também pode usá-lo para retornar logs de trabalho de um usuário específico ou de uma empresa e usuário.

**Solicitação**

```java
<ns1:getJobLogsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getJobLogsParam>
```

**Resposta**

```java
<getJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobLogArray>
      <items>
         <companyHandle>47</companyHandle>
         <jobHandle>47||Add_2007-09-14-15:04:34</jobHandle>
         <jobName>Add_2007-09-14-15:04:34</jobName>
         <submitUserEmail>kmagnusson@adobe.com</submitUserEmail>
         <logType>BeginUpload</logType>
         <startDate>2007-09-14T22:04:58.536-07:00</startDate>
         <fileSuccessCount>2</fileSuccessCount>
         <fileErrorCount>0</fileErrorCount>
         <fileWarningCount>205</fileWarningCount>
         <fileDuplicateCount>0</fileDuplicateCount>
         <fileUpdateCount>0</fileUpdateCount>
         <totalFileCount>0</totalFileCount>
         <fatalError>false</fatalError>
       </items>
   </jobLogArray>
</getJobLogsReturn>
```
