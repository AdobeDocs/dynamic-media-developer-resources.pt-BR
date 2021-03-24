---
description: Pausa um trabalho ativo.
solution: Experience Manager
title: pauseJob
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
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
