---
description: Essas operações novas ou modificadas e os tipos de dados disponíveis no WSDL beta não devem ser usados fora dos aplicativos desenvolvidos pela Dynamic Media.
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

Essas operações novas ou modificadas e os tipos de dados disponíveis no WSDL beta não devem ser usados fora dos aplicativos desenvolvidos pela Dynamic Media.

Essas operações e tipos estão sujeitos a desativação, alteração ou desativação com atualizações de sistema subsequentes.

**Novos tipos**

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

* Alterado `ActiveJob` para incluir um `createVideoSitemapJob` type

* Alterado `ScheduledJob` para incluir um `createVideoSitemapJob` type

* Alterado `ImageServingPublishJob` para incluir uma `contextHandle`

* Alterado `ImageRenderingPublishJob` para incluir uma `contextHandle`

* Alterado `MetadataField` para incluir uma `initialTagField`

* Alterado `MetadataCondition` para incluir e opcional `caseSensitive` parâmetro

* Alterado `PropertySet` para incluir uma `PermissionArray` as `permissions`

* Alterado `UploadDirectoryJob` para incluir opcionais `xmpKeywords`, `xmpTemplateId` e `xmpTemplateOverride` parâmetros

* Alterado `VideoPublishJob` para incluir uma `contextHandle`

**Operações Modificadas**

* Alterado `createAssetSet` para incluir uma `thumbAssetHandle`

* Alterado `createImageSet` para incluir uma `thumbAssetHandle`

* Alterado `createMetadataField` para incluir uma `initialTagValue` parâmetro

* Alterado `createPropertySet` para incluir uma `PermissionUpdateArray` as `permissionArray`

* Alterado `getImageServingPublishSettings` para incluir uma `contextHandle` parâmetro

* Alterado `getImageRenderingPublishSettings` para incluir uma `contextHandle` parâmetro

* Alterado `searchAssetsByFullText` para incluir uma série de parâmetros opcionais:

   * `SearchFilter` as `filters` parâmetro

   * `sortBy`
   * `sortDirection`

* Alterado `searchAssetsByMetadata` para incluir uma série de parâmetros opcionais:

   * `SearchFilter` as `filters` parâmetro

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` sequência de sete parâmetros

* Alterado `setAssetPublishState` para incluir uma `HandleArray` as `contextHandleArray`

* Alterado `setImageServingPublishSettings` para incluir uma `contextHandle` parâmetro

* Alterado `setImageRenderingPublishSettings` para incluir uma `contextHandle`parâmetro

* Alterado `submitJob` para incluir uma `createVideoSitemap` tipo de tarefa
