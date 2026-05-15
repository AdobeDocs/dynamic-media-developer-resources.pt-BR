---
description: Reinicia um trabalho pausado.
solution: Experience Manager
title: resumeJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ba8818ff-3040-463c-80d3-b7cfd1e01f77
TQID: 'https://experienceleague.adobe.com/WfYbUF7V5-cFK0wwvjPEAVEQc5SHiDiTqU-yBVaQoKg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 67
ht-degree: 0%

---

# resumeJob{#resumejob}

Reinicia um trabalho pausado.

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
| companyHandle | `xsd:string` | Sim | O identificador da empresa com o trabalho que você deseja reiniciar. |
| jobHandle | `xsd:string` | Sim | O identificador do trabalho pausado. |

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
