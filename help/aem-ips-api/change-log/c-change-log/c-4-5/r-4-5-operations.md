---
description: Descreve métodos de operações novos e alterados para a API do IPS versão 4.5.
solution: Experience Manager
title: Operações novas e modificadas
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---

# Operações: Novo e modificado{#operations-new-and-modified}

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

## Operações modificadas {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` inclui  `animatedGifInfo`,  `swcInfo`,  `cssInfo`e  `javascriptInfo` parâmetros.

* `createMetadataField` inclui um  `isHidden` parâmetro opcional .

* `saveMetadataField` inclui um  `isHidden` parâmetro opcional .

* `searchAssets`
* 
* O parâmetro `renameFiles` foi preterido para versões anteriores e removido da operação `renameAsset`. O caminho do arquivo virtual é alterado para corresponder ao novo nome do ativo (preservando a extensão do arquivo), enquanto os caminhos de arquivo físico não são afetados. Os clientes da API precisam remover referências a esse parâmetro ao atualizar para a nova versão da API.
