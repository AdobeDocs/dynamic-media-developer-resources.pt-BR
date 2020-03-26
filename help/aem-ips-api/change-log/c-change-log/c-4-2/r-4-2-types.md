---
description: Descreve tipos de dados novos e alterados para a API IPS versão 4.2.
seo-description: Descreve tipos de dados novos e alterados para a API IPS versão 4.2.
seo-title: Tipos de dados novos e modificados
solution: Experience Manager
title: Tipos de dados novos e modificados
topic: Scene7 Image Production System API
uuid: 274e49da-9eb8-4082-971c-056acb47a53e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

