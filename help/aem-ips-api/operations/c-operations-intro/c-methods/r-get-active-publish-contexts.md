---
description: Obtém uma lista de contextos de publicação ativos para a empresa especificada. Um contexto de publicação é considerado ativo se houver pelo menos um servidor ativo definido para o contexto.
solution: Experience Manager
title: getAtivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '108'
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
| companyHandle | `xsd:string` | Sim | O identificador da empresa para consultar contextos de publicação ativos |

**Saída (getActivePublishContextsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| contextArray | `types:StringArray` | Sim | A matriz de contextos de publicação ativos, que pode incluir zero ou mais valores do Contexto de publicação. |
