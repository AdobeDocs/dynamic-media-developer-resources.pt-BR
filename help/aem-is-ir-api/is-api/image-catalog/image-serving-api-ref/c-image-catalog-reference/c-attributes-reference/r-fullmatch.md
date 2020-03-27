---
description: Opção de correspondência de catálogo.
seo-description: Opção de correspondência de catálogo.
seo-title: FullMatch
solution: Experience Manager
title: FullMatch
topic: Scene7 Image Serving - Image Rendering API
uuid: 0c69ba92-1411-4cb7-ac28-d26fe035222f
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# FullMatch{#fullmatch}

Opção de correspondência de catálogo.

Uma entrada de catálogo é especificada como um par ` *``*/ *`rootIdimageId`*` em solicitações HTTP. Ao analisar, um catálogo será selecionado se ` *`rootId`*` corresponder ao `attribute::RootId` valor do catálogo e o registro do catálogo for identificado pela correspondência de ` *`imageId`*` com um `catalog::Id` valor. Se um catálogo for encontrado, mas não houver uma entrada de catálogo correspondente a ` *`imageId`*`, o servidor poderá fazer uma das seguintes ações:

Se não `attribute::FullMatch` estiver definido, o servidor usará os atributos do catálogo correspondente. Nesse caso, ` *`rootId`*` é substituído por `attribute::RootPath` (ou `default::RootPath`, se não for especificado neste catálogo).

Se `attribute::FullMatch` estiver definido, o servidor ignorará completamente o catálogo, como se nenhum catálogo tivesse sido correspondido, e continuará usando os atributos do catálogo padrão. Nesse caso, ` *`rootId`*` continua fazendo parte do caminho (que é anexado por `default::RootPath`).

## Propriedades {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Sinalizar. Defina como 0 para o comportamento padrão ou como 1 para ativar o comportamento de correspondência total.

## Padrão {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Herdado de `default::FullMatch` se não estiver definido ou se estiver vazio.

## Consulte também {#section-42da0ba53e0b4c089c62108785faf5a9}

[atributo::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catálogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
