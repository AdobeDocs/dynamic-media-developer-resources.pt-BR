---
description: Obtém os logs de trabalho de um ativo. Os itens retornados na matriz contêm informações detalhadas sobre cada entrada no registro de tarefas desse ativo. O campo de resposta logMessage está localizado com base no campo authHeader.
seo-description: Obtém os logs de trabalho de um ativo. Os itens retornados na matriz contêm informações detalhadas sobre cada entrada no registro de tarefas desse ativo. O campo de resposta logMessage está localizado com base no campo authHeader.
seo-title: getAssetJobLogs
solution: Experience Manager
title: getAssetJobLogs
topic: Dynamic Media Image Production System API
uuid: 7ea81baf-769b-4c73-bbc6-f52c89c98d50
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---


# getAssetJobLogs{#getassetjoblogs}

Obtém os logs de trabalho de um ativo. Os itens retornados na matriz contêm informações detalhadas sobre cada entrada no registro de tarefas desse ativo. O campo de resposta logMessage está localizado com base no campo authHeader.

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
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa à qual o ativo pertence. |
| `*`assetHandle`*` | `xsd:string` | Sim | O identificador para o ativo com os logs de trabalho a serem recuperados. |

**Saída (getAssetJobLogsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`jobLogArray`*` | `types:AssetJobLogArray` | Sim | Matriz de log de trabalhos. |

## Exemplos {#section-f03d7f3ec5d043d38227f926fb7609f6}

Essa amostra de código recupera os logs de trabalho de um ativo específico. A resposta retorna um storage de log de trabalhos com informações detalhadas sobre todos os trabalhos em que o ativo foi usado.

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

