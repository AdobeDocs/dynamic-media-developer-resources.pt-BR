---
description: Descreve tipos novos e alterados para a API IPS versão 6.
solution: Experience Manager
title: Tipos de dados Novo e Modificado
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# Tipos de dados: Novo e modificado{#data-types-new-and-modified}

Descreve tipos novos e alterados para a API IPS versão 6.

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

* Adição de `numUrls` a `UploadUrlsJob`.

* Adição de `fileName` a `Asset.`

* Adição de `isHidden` a `MetadataField`.

* Adição de `taskState` a `TaskProgress`.

* Adição de `exportJob` a `ActiveJob` e `ScheduledJob`.

* Adição de `optmizedPath` e `optimizedFile` a `PsdInfo`.

* Adição de `contextHandle` a:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Os seguintes parâmetros foram adicionados a `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Alterado**

* Em `User`, alterado `role` para `defaultRole`.

* Em `Folder`, alterado `permissions` para `permissionsSetHandle`.

* Em `AssetSummary`, `type` e `name` agora são opcionais.
