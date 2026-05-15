---
description: Descreve métodos de operações novos e alterados para a API do IPS versão 6.
solution: Experience Manager
title: Operações Novas e Modificadas
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
TQID: 'https://experienceleague.adobe.com/DLA26IsxxpZ0TSSfQBrvZSl8mbcJCaTfnpK-bhhmglg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 0%

---

# Operações: Novas e Modificadas{#operations-new-and-modified}

Descreve métodos de operações novos e alterados para a API do IPS versão 6.

Sintaxe

## Novas operações {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## Operações Modificadas {#section-f4e8755527444266ae806e3f4c851ae6}

**Adicionado**

* Adicionado `isHidden` e `initialTagValue` a:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Adicionado `thumbAssetHandle` a:

   * `createImageSet`
   * `createAssetSet`

  Adicionado `companyHandle` a:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

  Adicionado `contextHandle` a:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`

* Inclusão de includeInative adicionada a:

   * `getUsers`.
   * `getUserChars`.

* Adicionado `permissionArray` a `createPropertySet`.

* Adicionado `exportJob` a `submitJob`.

**Alterado**

* Em `addUser` e `setUser`, alterado `role` para `defaultRole`.

* Em `getCompanyMembers`, alterado `userArray` para `memberArray`.

* Em `getCompanyMembership`, alterado `companyArray` para `membershipArray`.

* Em `addUser`, `setCompanyMembership` e `addCompanyMembership`, mudou `membershipArray` para `companyHandleArray`.

* Em `getCompanyMembership`, alterado `companyArray` para `membershipArray`.

* Em `getUserChars`, `includeInvalid` agora é opcional.

**Removido**

* Removido `renameFiles` de `renameAsset`.

* Removido `getXMPPanelViewDefinition`.
* Removidos `searchAssetsByFulltext` e `searchAssetsBySimilarity`.
