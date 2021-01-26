---
description: Descreve métodos de operações novos e alterados para a API IPS versão 4.5.
solution: Experience Manager
title: Operações Novas e Modificadas
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---


# Operações: Novo e Modificado{#operations-new-and-modified}

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

* `Asset` inclui  `animatedGifInfo`,  `swcInfo`,  `cssInfo`e  `javascriptInfo` parâmetros.

* `createMetadataField` inclui um  `isHidden` parâmetro opcional.

* `saveMetadataField` inclui um  `isHidden` parâmetro opcional.

* `searchAssets`
* 
* O parâmetro `renameFiles` foi preterido para versões anteriores e removido da operação `renameAsset`. O caminho do arquivo virtual é alterado para corresponder ao novo nome do ativo (preservando a extensão do arquivo), enquanto os caminhos do arquivo físico não são afetados. Os clientes da API precisam remover referências a esse parâmetro ao atualizar para a nova versão da API.

