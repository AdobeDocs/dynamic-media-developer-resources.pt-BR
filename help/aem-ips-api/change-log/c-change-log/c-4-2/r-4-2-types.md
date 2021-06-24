---
description: Descreve tipos de dados novos e alterados para a API IPS versão 4.2.
solution: Experience Manager
title: Tipos de dados Novo e Modificado
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 0%

---

# Tipos de dados: Novo e modificado{#data-types-new-and-modified}

Descreve tipos de dados novos e alterados para a API IPS versão 4.2.

Sintaxe

## Novos tipos {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## Tipos modificados {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**Ativo**

Parâmetros adicionados:

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

Parâmetros removidos:

* `ImageSetInfo`
* `RenderSetInfo`

**ReprocessAssetsJob**

Parâmetros adicionados:

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectoryJob**

Parâmetros adicionados:

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

Parâmetros adicionados:

* `preservePublishState`
* `preserveCrop`
