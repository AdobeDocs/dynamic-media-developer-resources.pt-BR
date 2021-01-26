---
description: Descreve métodos de operações novos e alterados para a API IPS versão 6.
solution: Experience Manager
title: Operações Novas e Modificadas
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---


# Operações: Novo e Modificado{#operations-new-and-modified}

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

* Adicionados `isHidden` e `initialTagValue` a:

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

* Em `addUser` e `setUser`, `role` foram alteradas para `defaultRole`.

* Em `getCompanyMembers`, `userArray` foi alterado para `memberArray`.

* Em `getCompanyMembership`, `companyArray` foi alterado para `membershipArray`.

* Em `addUser`, `setCompanyMembership` e `addCompanyMembership`, `membershipArray` foram alteradas para `companyHandleArray`.

* Em `getCompanyMembership`, `companyArray` foi alterado para `membershipArray`.

* Em `getUserChars`, `includeInvalid` agora é opcional.

**Removido**

* Removido `renameFiles` de `renameAsset`.

* Removido `getXMPPanelViewDefinition`.
* Removidos `searchAssetsByFulltext` e `searchAssetsBySimilarity`.

