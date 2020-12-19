---
description: Descreve tipos novos e alterados para a API IPS versão 6.
seo-description: Descreve tipos novos e alterados para a API IPS versão 6.
seo-title: Tipos de dados novos e modificados
solution: Experience Manager
title: Tipos de dados novos e modificados
topic: Scene7 Image Production System API
uuid: ef7c43ee-467f-46b9-bd82-05e8359bd829
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '84'
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

