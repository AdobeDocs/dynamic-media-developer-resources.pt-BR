---
description: Descreve métodos de operações novos e alterados para a API do IPS versão 4.5.
solution: Experience Manager
title: Operações - Novas e Modificadas
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# Operações: Novas e Modificadas{#operations-new-and-modified}

Descreve métodos de operações novos e alterados para a API do IPS versão 4.5.

Sintaxe

## Novas operações {#section-a3be679d8e9345aba2e97699c3a537b9}

* `addMediaPortalEvent`
* `addTagFieldValues`
* `cdnCacheInvalidation`
* `deleteTagFieldValues`
* `deleteTagFieldValues`
* `getDistinctMetadataValues`
* `getMediaPortalEvent`
* `getTagFieldValues`
* `getXMPPacket`
* `searchAssetsByFullText`
* `searchAssetsByMetadata`
* `setTagFieldValues`
* `updateTagFieldValues`
* `updateXMPPacket`

## Operações Modificadas {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` inclui `animatedGifInfo`, `swcInfo`, `cssInfo`, e `javascriptInfo` parâmetros.
* `createMetadataField` inclui uma `isHidden` parâmetro.
* `saveMetadataField` inclui uma `isHidden` parâmetro.
* `searchAssets`
* A variável `renameFiles` foi descontinuado para versões anteriores e removido do `renameAsset` operação. O caminho do arquivo virtual é alterado para corresponder ao novo nome do ativo (preservando a extensão do arquivo), enquanto os caminhos do arquivo físico não são afetados. Os clientes da API precisam remover as referências a esse parâmetro ao atualizar para a nova versão da API.
