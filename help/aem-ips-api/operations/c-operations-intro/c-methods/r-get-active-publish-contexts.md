---
description: Obtém uma lista de contextos de publicação ativos para a empresa especificada. Um contexto de publicação é considerado ativo se houver pelo menos um servidor ativo definido para o contexto.
seo-description: Obtém uma lista de contextos de publicação ativos para a empresa especificada. Um contexto de publicação é considerado ativo se houver pelo menos um servidor ativo definido para o contexto.
seo-title: getActivePublishContext
solution: Experience Manager
title: getActivePublishContext
topic: Scene7 Image Production System API
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# getActivePublishContext{#getactivepublishcontext}

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

**Entrada (getActivePublishContextParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa para query para contextos de publicação ativos |

**Saída (getActivePublishContextReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`contextArray`*` | `types:StringArray` | Sim | A matriz de contextos de publicação ativos, que podem incluir zero ou mais valores do Contexto de publicação. |

