---
description: Pausa um trabalho ativo.
seo-description: Pausa um trabalho ativo.
seo-title: pauseJob
solution: Experience Manager
title: pauseJob
topic: Dynamic Media Image Production System API
uuid: baad2ad6-46f5-4133-a6d9-8ffadf990a06
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
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
| `*`companyHandle`*` | `xsd:string` | Sim | Segure a empresa. |
| `*`jobHandle`*` | `xsd:string` | Sim | Manipule o trabalho que deseja pausar. |

**Saída (PauseJobReturn)**

A API IPS não retorna uma resposta para esta operação.

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
