---
description: Obtém trabalhos agendados para execução.
seo-description: Obtém trabalhos agendados para execução.
seo-title: getScheduledJobs
solution: Experience Manager
title: getScheduledJobs
topic: Dynamic Media Image Production System API
uuid: 56b0623b-46d7-4d11-8eea-6543ed364b53
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---


# getScheduledJobs{#getscheduledjobs}

Obtém trabalhos agendados para execução.

Sintaxe

## Tipos de usuário autorizados {#section-bd1835ab508a429f8143b3bdb811d6a4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-2af604ff8282460990b9237158187f8f}

**Entrada (getScheduledJobsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | A alça da empresa. |
| `*`jobHandle`*` | `xsd:string` | Não | Trabalho. |
| `*`originalName`*` | `xsd:string` | Não | O nome especificado por `submitJob`. |

**Saída (getScheduledJobsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`jobArray`*` | `types:ScheduledJobArray` | Sim | Matriz de trabalhos agendados. |

## Exemplos {#section-e79e7da86ba848fd9996aa36de462e6c}

Esta amostra de código retorna todos os trabalhos agendados em uma matriz de trabalhos. O próprio storage contém informações detalhadas sobre os trabalhos.

**Solicitação**

```java
<getScheduledJobsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>0</companyHandle>
</getScheduledJobsParam>
```

**Resposta**

```java
<getScheduledJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray>
      <items>
         <companyHandle>0</companyHandle>
         <jobHandle>0|Cleanup|</jobHandle>
         <name>Cleanup</name>
         <originalName></originalName>
         <type>Cleanup</type>
         <submitUserEmail>default@scene7.com</submitUserEmail>
         <execSchedule>00 00 00 * * </execSchedule>
         <nextFireTime>2007-10-13T00:00:00.000-07:00</nextFireTime>
         <timeZone>PST</timeZone>
         <triggerState>Paused</triggerState>
      </items>
   </jobArray>
</getScheduledJobsReturn>
```

