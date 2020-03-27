---
description: Descreve métodos de operações novos e alterados para a API IPS versão 4.5.
seo-description: Descreve métodos de operações novos e alterados para a API IPS versão 4.5.
seo-title: Operações Novas e Modificadas
solution: Experience Manager
title: Operações Novas e Modificadas
topic: Scene7 Image Production System API
uuid: c4002670-c830-474e-bb84-343f76b6fb80
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Operações: Novo e modificado{#operations-new-and-modified}

Descreve métodos de operações novos e alterados para a API IPS versão 4.5.

Sintaxe

## Novas Operações {#section-a3be679d8e9345aba2e97699c3a537b9}

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

* `Asset` inclui `animatedGifInfo`, `swcInfo`, `cssInfo`e `javascriptInfo` parâmetros.

* `createMetadataField` inclui um `isHidden` parâmetro opcional.

* `saveMetadataField` inclui um `isHidden` parâmetro opcional.

* `searchAssets`
* 
* O `renameFiles` parâmetro foi descontinuado para versões anteriores e removido da `renameAsset` operação. O caminho do arquivo virtual é alterado para corresponder ao novo nome do ativo (preservando a extensão do arquivo), enquanto os caminhos do arquivo físico não são afetados. Os clientes da API precisam remover referências a esse parâmetro ao atualizar para a nova versão da API.

