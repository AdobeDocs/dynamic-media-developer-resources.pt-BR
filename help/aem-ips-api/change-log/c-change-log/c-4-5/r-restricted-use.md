---
description: Essas operações novas ou modificadas e os tipos de dados disponíveis no WSDL beta não devem ser usados fora dos aplicativos desenvolvidos pela Dynamic Media.
solution: Experience Manager
title: Uso restrito
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# Uso restrito{#restricted-use}

Essas operações novas ou modificadas e os tipos de dados disponíveis no WSDL beta não devem ser usados fora dos aplicativos desenvolvidos pela Dynamic Media.

Essas operações e tipos estão sujeitas à desativação, alteração ou descontinuação de atualizações subsequentes do sistema.

**Novos tipos**

* AtivoPublicarContextos
* AssetPublishContextsArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* PublicarContexto
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
* searchAssetsBySimilaridade
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**Tipos modificados**

* Alteração `ActiveJob` para incluir um tipo `createVideoSitemapJob`

* Alteração `ScheduledJob` para incluir um tipo `createVideoSitemapJob`

* `ImageServingPublishJob` alterado para incluir um `contextHandle` opcional

* `ImageRenderingPublishJob` alterado para incluir um `contextHandle` opcional

* `MetadataField` alterado para incluir um `initialTagField` opcional

* Alteração `MetadataCondition` para incluir e `caseSensitive` parâmetro opcional

* `PropertySet` alterado para incluir um `PermissionArray` opcional como `permissions`

* Alteração `UploadDirectoryJob` para incluir parâmetros opcionais `xmpKeywords`, `xmpTemplateId` e `xmpTemplateOverride`

* `VideoPublishJob` alterado para incluir um `contextHandle` opcional

**Operações modificadas**

* `createAssetSet` alterado para incluir um `thumbAssetHandle` opcional

* `createImageSet` alterado para incluir um `thumbAssetHandle` opcional

* `createMetadataField` alterado para incluir um parâmetro `initialTagValue` opcional

* `createPropertySet` alterado para incluir um `PermissionUpdateArray` opcional como `permissionArray`

* `getImageServingPublishSettings` alterado para incluir um parâmetro `contextHandle` opcional

* `getImageRenderingPublishSettings` alterado para incluir um parâmetro `contextHandle` opcional

* `searchAssetsByFullText` alterado para incluir uma série de parâmetros opcionais:

   * `SearchFilter` como  `filters` parâmetro

   * `sortBy`
   * `sortDirection`

* `searchAssetsByMetadata` alterado para incluir uma série de parâmetros opcionais:

   * `SearchFilter` como  `filters` parâmetro

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` sequência de sete parâmetros

* `setAssetPublishState` alterado para incluir um `HandleArray` opcional como `contextHandleArray`

* `setImageServingPublishSettings` alterado para incluir um parâmetro `contextHandle` opcional

* `setImageRenderingPublishSettings` alterado para incluir um parâmetro `contextHandle`opcional

* `submitJob` alterado para incluir um tipo de trabalho `createVideoSitemap` opcional

