---
description: Obtém uma lista de contextos de publicação ativos para a empresa especificada. Um contexto de publicação é considerado ativo se houver pelo menos um servidor ativo definido para o contexto.
seo-description: Obtém uma lista de contextos de publicação ativos para a empresa especificada. Um contexto de publicação é considerado ativo se houver pelo menos um servidor ativo definido para o contexto.
seo-title: getAtivePublishContext
solution: Experience Manager
title: getAtivePublishContext
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# getAtivePublishContext{#getactivepublishcontext}

Obtém uma lista de contextos de publicação ativos para a empresa especificada. Um contexto de publicação é considerado ativo se houver pelo menos um servidor ativo definido para o contexto.

Sintaxe

## Tipos de usuário autorizados {#section-eb22397744434dfe92a59ffa2883c2e7}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-a4be4024e55c472fa6728faec9c5e048}

**Entrada (getAtivePublishContextsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa para consultar contextos de publicação ativos |

**Saída (getActivePublishContextsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`contextArray`*` | `types:StringArray` | Sim | A matriz de contextos de publicação ativos, que pode incluir zero ou mais valores do Contexto de publicação. |

