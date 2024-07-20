---
description: Descreve métodos de operações novos e alterados para a API do IPS versão 6.
solution: Experience Manager
title: Operações Novas e Modificadas
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
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
