---
description: Descreve tipos de dados novos e alterados para a API IPS versão 4.2.
solution: Experience Manager
title: Tipos de dados Novo e Modificado
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 0%

---


# Tipos de dados: Novo e Modificado{#data-types-new-and-modified}

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

