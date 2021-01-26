---
description: Exclui um trabalho atual ou programado.
seo-description: Exclui um trabalho atual ou programado.
seo-title: deleteJob
solution: Experience Manager
title: deleteJob
topic: Dynamic Media Image Production System API
uuid: c1109cae-a3ca-40db-b641-9a6fc116c964
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---


# deleteJob{#deletejob}

Exclui um trabalho atual ou programado.

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
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa à qual o trabalho pertence. |
| `*`jobHandle`*` | `xsd:string` | Sim | O identificador do trabalho a ser excluído. |

**Saída**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Esta amostra de código exclui um trabalho que está em execução ou está programado para execução no IPS. Ela requer um identificador de trabalho, que você deve obter de outra operação.

**Solicitação**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Resposta**

Nenhum.
