---
description: Descreve tipos de dados novos e alterados para a API IPS versão 4.5.
seo-description: Descreve tipos de dados novos e alterados para a API IPS versão 4.5.
seo-title: Tipos de dados novos e modificados
solution: Experience Manager
title: Tipos de dados novos e modificados
topic: Scene7 Image Production System API
uuid: 2752f9dd-ec47-45d6-a465-6d275ec2b2fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Tipos de dados: Novo e modificado{#data-types-new-and-modified}

Descreve tipos de dados novos e alterados para a API IPS versão 4.5.

Sintaxe

## Novos tipos {#section-6941b228cf6747a987e98c3d6e4b6b17}

* `AssetSummary`
* `AssetSummaryArray`
* `JobLogDetailAux`
* `JobLogDetailAuxArray`
* `MPEvent`
* `MPEventArray`
* `OperationFault`
* `OperationFaultArray`
* `PhotoshopOptions`
* `TagCondition`
* `TagConditionArray`
* `TagFieldValues`
* `TagFieldValuesArray`
* `TagValueUpdate`
* `TagValueUpdateArray`
* `TagValueUpdateFault`
* `TagValueUpdateFaultArray`
* `UrlArray`

## Tipos modificados {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* O ativo inclui um novo `fileName` campo que retorna o nome do arquivo virtual.
* `AssetSummary` retorna um campo `type` e `name`

* `MetadataField` inclui `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` requer um `urlArray` e adiciona uma `numUrls` contagem opcional

