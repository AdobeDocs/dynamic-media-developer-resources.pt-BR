---
description: Descreve tipos de dados novos e alterados para a API IPS versão 4.5.
solution: Experience Manager
title: Tipos de dados Novo e Modificado
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# Tipos de dados: Novo e Modificado{#data-types-new-and-modified}

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

* O ativo inclui um novo campo `fileName` que retorna o nome do arquivo virtual.
* `AssetSummary` retorna um  `type` campo  `name` e

* `MetadataField` inclui  `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` requer um  `urlArray` e adiciona uma  `numUrls` contagem opcional

