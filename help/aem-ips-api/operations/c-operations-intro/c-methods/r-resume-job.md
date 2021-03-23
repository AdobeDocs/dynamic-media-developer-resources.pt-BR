---
description: Reinicializa um trabalho pausado.
seo-description: Reinicializa um trabalho pausado.
seo-title: resumeJob
solution: Experience Manager
title: resumeJob
uuid: 0ca5db75-cce0-4afc-9a58-c47c6229931e
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
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
