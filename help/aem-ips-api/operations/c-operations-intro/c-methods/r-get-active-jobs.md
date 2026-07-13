---
description: Obtém todos os trabalhos ativos no momento.
solution: Experience Manager
title: getActiveJobs
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 55e92ebc-d153-49b5-bf2e-c69d042e15b6
TQID: 'https://experienceleague.adobe.com/YTwzh2h9wVPuURKL5nNFoac2SruwYXDw9oWtd-vzowc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 101
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
| companyHandle | `xsd:string` | Não | O identificador da empresa. |
| jobHandle | `xsd:string` | Não | O identificador do trabalho. |
| originalName | `xsd:string` | Não | Nome do trabalho original. |

**Saída (getActiveJobsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| jobArray | `xsd:string` | Sim | Matriz de trabalhos ativos. |

## Exemplos {#section-4ac5dbbf9cd94fdeb013d055f8ee7add}

Esta amostra de código retorna todos os trabalhos ativos de uma empresa em execução no IPS. Nesse caso, a resposta é incomum porque o coordenador de agendamento do IPS está desativado sem tarefas ativas em execução. Em circunstâncias normais, a resposta retornaria uma série de trabalhos ativos.

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

