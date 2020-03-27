---
description: Interrompe um trabalho em andamento.
seo-description: Interrompe um trabalho em andamento.
seo-title: stopJob
solution: Experience Manager
title: stopJob
topic: Scene7 Image Production System API
uuid: 698c1652-5afa-4a2c-819a-1ba6ffc6aacf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Sim | Alça da Empresa. |
| ` *`jobHandle`*` | `xsd:string` | Sim | Lida com o trabalho que você quer parar. |

**Saída (stopJobReturn0**

A API IPS não retorna uma resposta para esta operação.

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
