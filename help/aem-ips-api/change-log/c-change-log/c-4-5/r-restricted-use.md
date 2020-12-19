---
description: Essas operações novas ou modificadas e os tipos de dados disponíveis no WSDL beta não devem ser usados fora dos aplicativos desenvolvidos pela Scene7.
seo-description: Essas operações novas ou modificadas e os tipos de dados disponíveis no WSDL beta não devem ser usados fora dos aplicativos desenvolvidos pela Scene7.
seo-title: Uso restrito
solution: Experience Manager
title: Uso restrito
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 0%

---


# Uso Restrito{#restricted-use}

Essas operações novas ou modificadas e os tipos de dados disponíveis no WSDL beta não devem ser usados fora dos aplicativos desenvolvidos pela Scene7.

Essas operações e tipos estão sujeitos a desativação, alteração ou desaprovação com atualizações subsequentes do sistema.

**Novos tipos**

* AssetPublishContext
* AssetPublishContextArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* PublicarContexto
* PublishContextArray
* SearchFilter
* LongArray

**Novas Operações**

* applyMetadataTemplate
* batchGetAssetPublishContext
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContext
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsBySimilities
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**Tipos modificados**

* Alteração de `ActiveJob` para incluir um tipo `createVideoSitemapJob`

* Alteração de `ScheduledJob` para incluir um tipo `createVideoSitemapJob`

* Alterado `ImageServingPublishJob` para incluir um `contextHandle` opcional

* Alterado `ImageRenderingPublishJob` para incluir um `contextHandle` opcional

* Alterado `MetadataField` para incluir um `initialTagField` opcional

* Alterado `MetadataCondition` para incluir e opcional parâmetro `caseSensitive`

* Alterado `PropertySet` para incluir um `PermissionArray` opcional como `permissions`

* Alteração `UploadDirectoryJob` para incluir os parâmetros opcionais `xmpKeywords`, `xmpTemplateId` e `xmpTemplateOverride`

* Alterado `VideoPublishJob` para incluir um `contextHandle` opcional

**Operações Modificadas**

* Alterado `createAssetSet` para incluir um `thumbAssetHandle` opcional

* Alterado `createImageSet` para incluir um `thumbAssetHandle` opcional

* Alterado `createMetadataField` para incluir um parâmetro `initialTagValue` opcional

* Alterado `createPropertySet` para incluir um `PermissionUpdateArray` opcional como `permissionArray`

* Alterado `getImageServingPublishSettings` para incluir um parâmetro `contextHandle` opcional

* Alterado `getImageRenderingPublishSettings` para incluir um parâmetro `contextHandle` opcional

* `searchAssetsByFullText` alterado para incluir uma série de parâmetros opcionais:

   * `SearchFilter` como  `filters` parâmetro

   * `sortBy`
   * `sortDirection`

* `searchAssetsByMetadata` alterado para incluir uma série de parâmetros opcionais:

   * `SearchFilter` como  `filters` parâmetro

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` sequência de sete parâmetros

* Alterado `setAssetPublishState` para incluir um `HandleArray` opcional como `contextHandleArray`

* Alterado `setImageServingPublishSettings` para incluir um parâmetro `contextHandle` opcional

* Alterado `setImageRenderingPublishSettings` para incluir um parâmetro `contextHandle`opcional

* Alterado `submitJob` para incluir um tipo de trabalho `createVideoSitemap` opcional

