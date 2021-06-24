---
description: Pausa um trabalho ativo.
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 010e969a-911e-49fc-8577-66c18cd4329c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 0%

---

# pauseJob{#pausejob}

Pausa um trabalho ativo.

Sintaxe

## Tipos de usuário autorizados {#section-f2bf306ab4574871bd21f9f7dd681033}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-7aedb924cf8b4e05a0dc927636d537a0}

**Entrada (pauseJobParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Manipule a empresa. |
| `*`jobHandle`*` | `xsd:string` | Sim | Manipule o trabalho que deseja pausar. |

**Saída (PauseJobReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-ee4914f9496f4bd88556728a48fb22c1}

Esta amostra de código pausa um trabalho ativo.

**Solicitação**

```java
<pauseJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</pauseJobParam>
```

**Resposta**

Nenhum.
