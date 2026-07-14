---
description: Obtém os trabalhos agendados para execução.
solution: Experience Manager
title: getScheduledJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7920637e-b289-410c-ae5c-e67cd7b21aba
TQID: 'https://experienceleague.adobe.com/DNUaAhcCeO8MvLH5YF5-WTA74fCyRKLxvXBKu0ltngk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 75
ht-degree: 0%

---

# getScheduledJobs{#getscheduledjobs}

Obtém os trabalhos agendados para execução.

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
| companyHandle | `xsd:string` | Sim | O identificador da empresa. |
| jobHandle | `xsd:string` | Não | Identificador do trabalho. |
| originalName | `xsd:string` | Não | O nome especificado por `submitJob`. |

**Saída (getScheduledJobsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| jobArray | `types:ScheduledJobArray` | Sim | Matriz de trabalhos agendados. |

## Exemplos {#section-e79e7da86ba848fd9996aa36de462e6c}

Esta amostra de código retorna todos os trabalhos agendados em uma matriz de trabalhos. A própria matriz contém informações detalhadas sobre os trabalhos.

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

