---
description: Descreve tipos novos e alterados para a API do IPS versão 6.
solution: Experience Manager
title: Tipos de dados novos e modificados
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d3bcd718-cf27-4d31-850f-a3205564be60
TQID: 'https://experienceleague.adobe.com/LI8xzlS2eACzYqcV3krzThLm77-z6imYLohPRCTHIYs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
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

* Adicionado `numUrls` a `UploadUrlsJob`.

* Adicionado `fileName` a `Asset.`

* Adicionado `isHidden` a `MetadataField`.

* Adicionado `taskState` a `TaskProgress`.

* Adicionado `exportJob` a `ActiveJob` e `ScheduledJob`.

* Adicionado `optmizedPath` e `optimizedFile` a `PsdInfo`.

* Adicionado `contextHandle` a:

   * `ImageRenderingPublishJob`
   * `VideoPublishJob`

* Adicionamos os seguintes parâmetros a `Asset`:

   * `animatedGifInfo`
   * `swcInfo`
   * `cssInfo`
   * `javascriptInfo`

**Alterado**

* Em `User`, alterado `role` para `defaultRole`.

* Em `Folder`, alterado `permissions` para `permissionsSetHandle`.

* Em `AssetSummary`, `type` e `name` agora são opcionais.
