---
description: Interrompe um trabalho em andamento.
solution: Experience Manager
title: stopJob
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '61'
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
