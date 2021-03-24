---
description: Obtém tarefas agendadas para execução.
solution: Experience Manager
title: getScheduledJobs
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---


# getScheduledJobs{#getscheduledjobs}

Obtém tarefas agendadas para execução.

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
| `*`companyHandle`*` | `xsd:string` | Sim | O nome da empresa. |
| `*`jobHandle`*` | `xsd:string` | Não | Identificador da tarefa. |
| `*`originalName`*` | `xsd:string` | Não | O nome especificado por `submitJob`. |

**Saída (getScheduledJobsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`jobArray`*` | `types:ScheduledJobArray` | Sim | Matriz de trabalhos agendados. |

## Exemplos {#section-e79e7da86ba848fd9996aa36de462e6c}

Esta amostra de código retorna todas as tarefas agendadas em uma matriz de tarefas. O próprio storage contém informações detalhadas sobre as tarefas.

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

