---
description: URL raiz para URLs de imagem relativos. Especifica a URL raiz para URLs de imagem relativas.
solution: Experience Manager
title: RootUrl
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 72560180-53e5-4293-9dd3-c0cd196551dc
TQID: 'https://experienceleague.adobe.com/c-jvMp3XvBjonacYBfmA7b8MnA83SKi2lsO9YJLPqis'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 0%

---

# RootUrl{#rooturl}

URL raiz para URLs de imagem relativos. Especifica a URL raiz para URLs de imagem relativas.

`attribute::RootUrl` é usado em vez de `attribute::RootPath` quando um valor `src=` ou `mask=` é delimitado por {curly braces} ou (parênteses).

## Propriedades {#section-fe02269b4b724319a5d1f2cfcae31cba}

Valor da string de texto. Caminho raiz absoluto do URL, incluindo o identificador de protocolo principal. Os seguintes protocolos são compatíveis: HTTP, HTTPS e FTP.

## Padrão {#section-fa5e3fc993c04086bc2b06dfeea4ae5c}

Herdado de `default::RootUrl` se não estiver definido. Se definidos, mas vazios, os URLs relativos não são compatíveis com esse catálogo de imagens.

## Consulte também {#section-ade4789086df4e76ae041cd4acfa2f85}

[src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1) , [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [attribute:RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)
