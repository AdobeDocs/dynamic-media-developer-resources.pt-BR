---
description: Essas operações novas ou modificadas e os tipos de dados disponíveis no WSDL beta não devem ser usados fora dos aplicativos desenvolvidos pelo Dynamic Media.
solution: Experience Manager
title: Uso restrito
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# Uso restrito{#restricted-use}

Essas operações novas ou modificadas e os tipos de dados disponíveis no WSDL beta não devem ser usados fora dos aplicativos desenvolvidos pelo Dynamic Media.

Essas operações e tipos estão sujeitos a desativação, alteração ou desativação com atualizações de sistema subsequentes.

**Novos Tipos**

* AssetPublishContexts
* AssetPublishContextsArray
* InformaçõesDeMetadadosDaEmpresa
* MatrizInfoMetadadosEmpresa
* CreateVideoSitemapJob
* PublishContext
* PublishContextArray
* SearchFilter
* LongArray

**Novas operações**

* applyMetadataTemplate
* batchGetAssetPublishContexts
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContexts
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsBySimilarity
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**Tipos modificados**

* Alterou `ActiveJob` para incluir um tipo `createVideoSitemapJob`

* Alterou `ScheduledJob` para incluir um tipo `createVideoSitemapJob`

* Alterou `ImageServingPublishJob` para incluir um `contextHandle` opcional

* Alterou `ImageRenderingPublishJob` para incluir um `contextHandle` opcional

* Alterou `MetadataField` para incluir um `initialTagField` opcional

* Alterou `MetadataCondition` para incluir e parâmetro `caseSensitive` opcional

* Alterou `PropertySet` para incluir um `PermissionArray` opcional como `permissions`

* Alterou `UploadDirectoryJob` para incluir parâmetros `xmpKeywords`, `xmpTemplateId` e `xmpTemplateOverride` opcionais

* Alterou `VideoPublishJob` para incluir um `contextHandle` opcional

**Operações Modificadas**

* Alterou `createAssetSet` para incluir um `thumbAssetHandle` opcional

* Alterou `createImageSet` para incluir um `thumbAssetHandle` opcional

* Alterou `createMetadataField` para incluir um parâmetro `initialTagValue` opcional

* Alterou `createPropertySet` para incluir um `PermissionUpdateArray` opcional como `permissionArray`

* Alterou `getImageServingPublishSettings` para incluir um parâmetro `contextHandle` opcional

* Alterou `getImageRenderingPublishSettings` para incluir um parâmetro `contextHandle` opcional

* Alterado `searchAssetsByFullText` para incluir uma série de parâmetros opcionais:

   * `SearchFilter` como parâmetro `filters`

   * `sortBy`
   * `sortDirection`

* Alterado `searchAssetsByMetadata` para incluir uma série de parâmetros opcionais:

   * `SearchFilter` como parâmetro `filters`

   * `sortBy`
   * `sortDirection`
   * Sequência `haystackSearch` de sete parâmetros

* Alterou `setAssetPublishState` para incluir um `HandleArray` opcional como `contextHandleArray`

* Alterou `setImageServingPublishSettings` para incluir um parâmetro `contextHandle` opcional

* Alterou `setImageRenderingPublishSettings` para incluir um parâmetro `contextHandle` opcional

* Alterou `submitJob` para incluir um tipo de trabalho `createVideoSitemap` opcional
