---
description: URL raiz para URLs de imagem relativos. Especifica o URL raiz para URLs de imagem relativos.
seo-description: URL raiz para URLs de imagem relativos. Especifica o URL raiz para URLs de imagem relativos.
seo-title: RootUrl
solution: Experience Manager
title: RootUrl
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 173ce99a-f87e-4700-a28a-1a87b8c55b85
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# RootUrl{#rooturl}

URL raiz para URLs de imagem relativos. Especifica o URL raiz para URLs de imagem relativos.

`attribute::RootUrl` é usado em vez de  `attribute::RootPath` quando um  `src=` ou  `mask=` valor é delimitado por {chaves} ou (parênteses).

## Propriedades {#section-fe02269b4b724319a5d1f2cfcae31cba}

Valor da string de texto. Caminho raiz absoluto do URL, incluindo o identificador de protocolo à esquerda. Os seguintes protocolos são suportados: HTTP, HTTPS e FTP.

## Padrão {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

Herdado de `default::RootUrl` se não estiver definido. Se definido, mas vazio, URLs relativos não são suportados por esse catálogo de imagens.

## Consulte também {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) ,  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [attribute:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [conjunto de regras::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
