---
description: Exclui um trabalho atual ou agendado.
solution: Experience Manager
title: deleteJob
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d38dd1e2-668e-4956-b854-54bf466d6d45
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 0%

---

# deleteJob{#deletejob}

Exclui um trabalho atual ou agendado.

Sintaxe

## Tipos de usuário autorizados {#section-1b959679dc8147c291126ddf7e061742}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-000c42bc93744b1a8e777f3ec3c272b0}

**Entrada (deleteJobParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa à qual o trabalho pertence. |
| jobHandle | `xsd:string` | Sim | O identificador do trabalho a ser excluído. |

**Saída**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Esta amostra de código exclui um trabalho que está em execução ou está agendado para execução no IPS. Requer um identificador de trabalho, que você deve obter de outra operação.

**Solicitação**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Resposta**

Nenhum.
