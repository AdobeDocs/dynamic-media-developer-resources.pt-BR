---
description: Exclui um trabalho atual ou programado.
seo-description: Exclui um trabalho atual ou programado.
seo-title: deleteJob
solution: Experience Manager
title: deleteJob
uuid: c1109cae-a3ca-40db-b641-9a6fc116c964
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '104'
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

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-732d21d4dad04337b7a5ae1a0cc00eba}

Esta amostra de código exclui um trabalho que está em execução ou está agendado para execução no IPS. Ele requer um identificador de trabalho, que deve ser obtido de outra operação.

**Solicitação**

```java
<deleteJobParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>47</companyHandle>
   <jobHandle>47|My Test Job|</jobHandle>
</deleteJobParam>
```

**Resposta**

Nenhum.
