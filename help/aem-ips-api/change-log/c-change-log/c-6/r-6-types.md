---
description: Descreve tipos novos e alterados para a API do IPS versão 6.
solution: Experience Manager
title: Tipos de dados novos e modificados
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 0%

---

# Tipos de dados: novos e modificados{#data-types-new-and-modified}

Descreve tipos novos e alterados para a API do IPS versão 6.

Sintaxe

## Novos tipos {#section-71ba6954339e4ba899acdf8a3212d6f3}

* `AssetContextStateUpdate`
* `AssetContextStateUpdateArray`
* `AssetPublishContexts`
* `AssetPublishContextsArray`
* `CompanyMember`
* `CompanyMemberArray`
* `CompanyMembershipUpdate`
* `CompanyMembershipUpdateArray`
* `ContextStateUpdate`
* `ContextStateUpdateArray`
* `Export Job`
* `PermissionsSet`
* `PermissionsSetArray`
* `PublishContext`
* `PublishContextArray`

## Tipos modificados {#section-56b834b1a3b843279d8715b4a4f3890b}

**Adicionado**

* Adicionado `numUrls` para `UploadUrlsJob`.

* Adicionado `fileName` para `Asset.`

* Adicionado `isHidden` para `MetadataField`.

* Adicionado `taskState` para `TaskProgress`.

* Adicionado `exportJob` para `ActiveJob` e `ScheduledJob`.

* Adicionado `optmizedPath` e `optimizedFile` para `PsdInfo`.

* Adicionado `contextHandle` para:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Adição dos seguintes parâmetros a `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Alterado**

* Entrada `User`, alterado `role` para `defaultRole`.

* Entrada `Folder`, alterado `permissions` para `permissionsSetHandle`.

* Entrada `AssetSummary`, `type` e `name` agora são opcionais.
