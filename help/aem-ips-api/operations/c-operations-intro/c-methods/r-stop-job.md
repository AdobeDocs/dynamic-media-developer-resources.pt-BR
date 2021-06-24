---
description: Interrompe um trabalho em andamento.
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 90e61cf1-11f1-4504-8007-126ba4fe436a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 0%

---

# stopJob{#stopjob}

Interrompe um trabalho em andamento.

Sintaxe

## Tipos de usuário autorizados {#section-b222f561143747f6ad089aadc0b274d8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-2b64f074e37c4c38849994f3bc65342a}

**Entrada (stopJobParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Manuseio da empresa. |
| `*`jobHandle`*` | `xsd:string` | Sim | Lide com o trabalho que deseja parar. |

**Saída (stopJobReturn0**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-f7e07fa09ae24dc89685533f20ab3b81}

**Solicitação**

```java
<stopJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</stopJobParam>
```

**Resposta**

Nenhum.
