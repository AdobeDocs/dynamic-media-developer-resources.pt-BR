---
description: Descreve tipos de dados novos e alterados para a API do IPS versão 4.2.
solution: Experience Manager
title: Tipos de dados novos e modificados
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
TQID: 'https://experienceleague.adobe.com/2YCgrii3dF6Zq7NlXRI0vD3DtO-jWpSo4YKcpZsdFHU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 53
ht-degree: 0%

---

# Tipos de dados: novos e modificados{#data-types-new-and-modified}

Descreve tipos de dados novos e alterados para a API do IPS versão 4.2.

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

