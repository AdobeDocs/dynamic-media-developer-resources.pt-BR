---
description: URL raiz para URLs de imagem relativos. Especifica a URL raiz para URLs de imagem relativas.
solution: Experience Manager
title: RootUrl
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72560180-53e5-4293-9dd3-c0cd196551dc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# RootUrl{#rooturl}

URL raiz para URLs de imagem relativos. Especifica a URL raiz para URLs de imagem relativas.

`attribute::RootUrl` é usado em vez de `attribute::RootPath` quando um `src=` ou `mask=` O valor está entre {curly braces} ou (parênteses).

## Propriedades {#section-fe02269b4b724319a5d1f2cfcae31cba}

Valor da string de texto. Caminho raiz absoluto do URL, incluindo o identificador de protocolo principal. Os seguintes protocolos são compatíveis: HTTP, HTTPS e FTP.

## Padrão {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

Herdado de `default::RootUrl` se não estiver definido. Se definidos, mas vazios, os URLs relativos não são compatíveis com esse catálogo de imagens.

## Consulte também {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [atributo:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [conjunto de regras::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
