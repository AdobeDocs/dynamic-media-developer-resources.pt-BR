---
description: Obtém todos os trabalhos ativos no momento.
seo-description: Obtém todos os trabalhos ativos no momento.
seo-title: getActiveJobs
solution: Experience Manager
title: getActiveJobs
topic: Dynamic Media Image Production System API
uuid: 3231d349-b254-4dd0-804d-8beaab116b56
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---


# getActiveJobs{#getactivejobs}

Obtém todos os trabalhos ativos no momento.

Sintaxe

## Tipos de usuário autorizados {#section-125557a6ea7b4fc894d4bb468cd02118}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-29018fba6bf34c1e80dcd479dd24f3b5}

**Entrada (getActiveJobsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Não | A alça da empresa. |
| `*`jobHandle`*` | `xsd:string` | Não | O controle do trabalho. |
| `*`originalName`*` | `xsd:string` | Não | Nome do trabalho original. |

**Saída (getActiveJobsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`jobArray`*` | `xsd:string` | Sim | Matriz de trabalhos ativos. |

## Exemplos {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

Esta amostra de código retorna todos os trabalhos ativos de uma empresa em execução no IPS. Nesse caso, a resposta é incomum porque o coordenador de agendamento do IPS está desabilitado sem trabalhos ativos em execução. Em circunstâncias normais, a resposta retornaria uma série de empregos ativos.

**Solicitação**

```java
<ns1:getActiveJobsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getActiveJobsParam>
```

**Resposta**

```java
<getActiveJobsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <jobArray></jobArray>
</getActiveJobsReturn>
```

