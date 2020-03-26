---
description: Essas operações novas ou modificadas e os tipos de dados disponíveis no WSDL beta não devem ser usados fora das aplicações desenvolvidas pelo Scene7.
seo-description: Essas operações novas ou modificadas e os tipos de dados disponíveis no WSDL beta não devem ser usados fora das aplicações desenvolvidas pelo Scene7.
seo-title: Uso restrito
solution: Experience Manager
title: Uso restrito
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Uso restrito{#restricted-use}

Essas operações novas ou modificadas e os tipos de dados disponíveis no WSDL beta não devem ser usados fora das aplicações desenvolvidas pelo Scene7.

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

* Alterado `ActiveJob` para incluir um `createVideoSitemapJob` tipo

* Alterado `ScheduledJob` para incluir um `createVideoSitemapJob` tipo

* Alterado `ImageServingPublishJob` para incluir um `contextHandle`

* Alterado `ImageRenderingPublishJob` para incluir um `contextHandle`

* Alterado `MetadataField` para incluir um `initialTagField`

* Alterado `MetadataCondition` para incluir e `caseSensitive` parâmetro opcional

* Alterado `PropertySet` para incluir uma opção `PermissionArray` como `permissions`

* Alterado `UploadDirectoryJob` para incluir `xmpKeywords`parâmetros opcionais `xmpTemplateId` e `xmpTemplateOverride`

* Alterado `VideoPublishJob` para incluir um `contextHandle`

**Operações Modificadas**

* Alterado `createAssetSet` para incluir um `thumbAssetHandle`

* Alterado `createImageSet` para incluir um `thumbAssetHandle`

* Alterado `createMetadataField` para incluir um `initialTagValue` parâmetro opcional

* Alterado `createPropertySet` para incluir uma opção `PermissionUpdateArray` como `permissionArray`

* Alterado `getImageServingPublishSettings` para incluir um `contextHandle` parâmetro opcional

* Alterado `getImageRenderingPublishSettings` para incluir um `contextHandle` parâmetro opcional

* Alterado `searchAssetsByFullText` para incluir uma série de parâmetros opcionais:

   * `SearchFilter` como `filters` parâmetro

   * `sortBy`
   * `sortDirection`

* Alterado `searchAssetsByMetadata` para incluir uma série de parâmetros opcionais:

   * `SearchFilter` como `filters` parâmetro

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` sequência de sete parâmetros

* Alterado `setAssetPublishState` para incluir uma opção `HandleArray` como `contextHandleArray`

* Alterado `setImageServingPublishSettings` para incluir um `contextHandle` parâmetro opcional

* Alterado `setImageRenderingPublishSettings` para incluir um `contextHandle`parâmetro opcional

* Alterado `submitJob` para incluir um tipo de `createVideoSitemap` trabalho opcional

