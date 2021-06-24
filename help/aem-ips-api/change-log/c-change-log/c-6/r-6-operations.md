---
description: Descreve métodos de operações novos e alterados para a API IPS versão 6.
solution: Experience Manager
title: Operações novas e modificadas
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---

# Operações: Novo e modificado{#operations-new-and-modified}

Descreve métodos de operações novos e alterados para a API IPS versão 6.

Sintaxe

## Novas operações {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## Operações modificadas {#section-f4e8755527444266ae806e3f4c851ae6}

**Adicionado**

* Adição de `isHidden` e `initialTagValue` a:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Adição de `thumbAssetHandle` a:

   * `createImageSet`
   * `createAssetSet`

   Adição de `companyHandle` a:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   Adição de `contextHandle` a:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* InclusãoInativa adicionada a:

   * `getUsers`.
   * `getUserChars`.

* Adição de `permissionArray` a `createPropertySet`.

* Adição de `exportJob` a `submitJob`.

**Alterado**

* Em `addUser` e `setUser`, foi alterado `role` para `defaultRole`.

* Em `getCompanyMembers`, alterado `userArray` para `memberArray`.

* Em `getCompanyMembership`, alterado `companyArray` para `membershipArray`.

* Em `addUser`, `setCompanyMembership` e `addCompanyMembership`, foram alteradas `membershipArray` para `companyHandleArray`.

* Em `getCompanyMembership`, alterado `companyArray` para `membershipArray`.

* Em `getUserChars`, `includeInvalid` agora é opcional.

**Removido**

* Remoção de `renameFiles` de `renameAsset`.

* Remoção de `getXMPPanelViewDefinition`.
* Remoção de `searchAssetsByFulltext` e `searchAssetsBySimilarity`.
