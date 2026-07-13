---
description: Obtém logs de trabalho especificados para a empresa selecionada. Você pode classificar por caracteres, direção, datas de início e término e número de linhas.
solution: Experience Manager
title: getJobLogs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6239c3c4-bdbc-4e69-82d4-48a76f080eff
TQID: 'https://experienceleague.adobe.com/lerbQ3ibPCI3zqkrmgPrwTAYp1w6dWxIWYRt2Ij51oA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 184
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

