---
description: Descreve tipos novos e alterados para a API IPS versão 6.
solution: Experience Manager
title: Tipos de dados novos e modificados
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 0%

---


# Tipos de dados: Novo e Modificado{#data-types-new-and-modified}

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

* Adicionado `numUrls` a `UploadUrlsJob`.

* Adicionado `fileName` a `Asset.`

* Adicionado `isHidden` a `MetadataField`.

* Adicionado `taskState` a `TaskProgress`.

* Adicionado `exportJob` a `ActiveJob` e `ScheduledJob`.

* Adicionados `optmizedPath` e `optimizedFile` a `PsdInfo`.

* Adicionado `contextHandle` a:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Os seguintes parâmetros foram adicionados a `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Alterado**

* Em `User`, `role` foi alterado para `defaultRole`.

* Em `Folder`, `permissions` foi alterado para `permissionsSetHandle`.

* Em `AssetSummary`, `type` e `name` agora são opcionais.

