---
description: Obtém os logs de trabalho de um ativo. Os itens retornados na matriz contêm informações detalhadas sobre cada entrada no log de tarefas desse ativo. O campo de resposta logMessage é localizado com base no campo authHeader.
solution: Experience Manager
title: getAssetJobLogs
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 88ec5cab-7eb4-48aa-914f-21311593e463
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---

# getAssetJobLogs{#getassetjoblogs}

Obtém os logs de trabalho de um ativo. Os itens retornados na matriz contêm informações detalhadas sobre cada entrada no log de tarefas desse ativo. O campo de resposta logMessage é localizado com base no campo authHeader.

Sintaxe

## Tipos de usuário autorizados {#section-72b98cdb0f6f47f5aabdc183a45ea577}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-9586617e124b4da4acb6b66b2a9adad8}

**Entrada (getAssetJobLogsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa à qual o ativo pertence. |
| assetHandle | `xsd:string` | Sim | O identificador do ativo com os logs de trabalho a serem recuperados. |

**Saída (getAssetJobLogsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| jobLogArray | `types:AssetJobLogArray` | Sim | Matriz de log de trabalho. |

## Exemplos {#section-f03d7f3ec5d043d38227f926fb7609f6}

Esta amostra de código recupera os logs de trabalho de um ativo específico. A resposta retorna uma matriz de logs de trabalho com informações detalhadas sobre todos os trabalhos nos quais o ativo foi usado.

**Solicitação**

```java
<getAssetJobLogsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetJobLogsParam>
```

**Resposta**

```java
<getAssetJobLogsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <jobLogArray>
      <items>
         <jobHandle>j|6||Add_2007-10-24-16:11:07</jobHandle>
         <jobName>Add_2007-10-24-16:11:07</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS</logMessage>
         <logType>UploadSuccess</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2007-10-24T16:12:32.297-07:00</logDate>
      </items>
      <items>
         <jobHandle>j|6||submitServerUploadJob40_2008-06-11-11:38</jobHandle>
         <jobName>submitServerUploadJob40_2008-06-11-11:38</jobName>
         <logMessage>ApiTestCo/blakexslttest.jpg was processed into IPS.</logMessage>
         <logType>FileUpdated</logType>
         <submitUserEmail>strangio@adobe.com</submitUserEmail>
         <logDate>2008-06-11T11:38:48.547-07:00</logDate>
      </items>
   </jobLogArray>
</getAssetJobLogsReturn>
```
