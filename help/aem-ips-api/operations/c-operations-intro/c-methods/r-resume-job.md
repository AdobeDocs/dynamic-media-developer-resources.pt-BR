---
description: Reinicializa um trabalho pausado.
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---

# resumeJob{#resumejob}

Reinicializa um trabalho pausado.

Sintaxe

## Tipos de usuário autorizados {#section-eab49f4b6d1041179000326a10fee889}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-6b2f8aa65d4d4ae1af0c9cee468b0a51}

**Entrada (resumeJobParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa com o trabalho que deseja reiniciar. |
| `*`jobHandle`*` | `xsd:string` | Sim | O identificador para o trabalho pausado. |

**Saída (resumeJobReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-d0524e031f1f43d89430eade19526162}

Esta amostra de código reinicia um trabalho pausado.

**Solicitação**

```java
<resumeJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</resumeJobParam>
```

**Resposta**

Nenhum.
