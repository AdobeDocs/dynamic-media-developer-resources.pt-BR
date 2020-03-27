---
description: Descreve métodos de operações novos e alterados para a API IPS versão 6.
seo-description: Descreve métodos de operações novos e alterados para a API IPS versão 6.
seo-title: Operações Novas e Modificadas
solution: Experience Manager
title: Operações Novas e Modificadas
topic: Scene7 Image Production System API
uuid: e36f0d5c-0170-4a65-9347-c7fd3538726b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Operações: Novo e modificado{#operations-new-and-modified}

Descreve métodos de operações novos e alterados para a API IPS versão 6.

Sintaxe

## Novas Operações {#section-088502a0746945f28a5ea100cd655bc6}

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



* Adicionado includeInative para:

   * `getUsers`.
   * `getUserChars`.

* Adicionado `permissionArray` a `createPropertySet`.

* Adicionado `exportJob` a `submitJob`.

**Alterado**

* Em `addUser` e `setUser`, mudei `role` para `defaultRole`.

* Em `getCompanyMembers`, mudei `userArray` para `memberArray`.

* Em `getCompanyMembership`, mudei `companyArray` para `membershipArray`.

* Em `addUser`, `setCompanyMembership`, e `addCompanyMembership`, mudei `membershipArray` para `companyHandleArray`.

* Em `getCompanyMembership`, mudei `companyArray` para `membershipArray`.

* Em `getUserChars`, `includeInvalid` agora é opcional.

**Removido**

* Removido `renameFiles` de `renameAsset`.

* Removido `getXMPPanelViewDefinition`.
* Removido `searchAssetsByFulltext` e `searchAssetsBySimilarity`.

