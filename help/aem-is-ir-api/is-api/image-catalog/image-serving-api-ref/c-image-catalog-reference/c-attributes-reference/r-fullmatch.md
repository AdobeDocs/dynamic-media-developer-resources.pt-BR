---
description: Opção de correspondência de catálogo.
solution: Experience Manager
title: CorrespondênciaCompleta
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# CorrespondênciaCompleta{#fullmatch}

Opção de correspondência de catálogo.

Uma entrada de catálogo é especificada como uma `*`rootId`*/ *`imageId`*` emparelhar em solicitações HTTP. Ao analisar, um catálogo é selecionado se `*`rootId`*` corresponde ao `attribute::RootId` valor do catálogo, e o registro do catálogo é identificado pela correspondência `*`imageId`*` com um `catalog::Id` valor. Se um catálogo for encontrado, mas não houver nenhuma entrada de catálogo correspondente `*`imageId`*`, o servidor pode executar uma das seguintes ações:

Se `attribute::FullMatch` não estiver definido, o servidor usará os atributos do catálogo correspondente. Nesse caso, `*`rootId`*` é substituída por `attribute::RootPath` (ou `default::RootPath`, se não especificado neste catálogo).

Se `attribute::FullMatch` for definido, o servidor ignorará completamente o catálogo, como se nenhum catálogo tivesse sido correspondido, e continuará usando os atributos de catálogo padrão. Nesse caso, `*`rootId`*` permanece parte do caminho (que é precedido por `default::RootPath`).

## Propriedades {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Sinalizador. Defina como 0 para comportamento padrão ou como 1 para ativar o comportamento de correspondência total.

## Padrão {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Herdado de `default::FullMatch` se não estiver definido ou se estiver vazio.

## Consulte também {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catálogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
