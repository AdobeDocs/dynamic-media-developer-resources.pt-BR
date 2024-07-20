---
description: Opção de correspondência de catálogo.
solution: Experience Manager
title: CorrespondênciaCompleta
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a267c48-a8eb-426a-a70a-bdb9f5f20efb
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---

# CorrespondênciaCompleta{#fullmatch}

Opção de correspondência de catálogo.

Uma entrada de catálogo é especificada como um par `*`rootId`*/ *`imageId`*` em solicitações HTTP. Durante a análise, um catálogo será selecionado se `*`rootId`*` corresponder ao valor `attribute::RootId` do catálogo, e o registro do catálogo será identificado pela correspondência de `*`imageId`*` com um valor `catalog::Id`. Se um catálogo for encontrado, mas não houver uma entrada de catálogo correspondente a `*`imageId`*`, o servidor poderá executar uma das seguintes ações:

Se `attribute::FullMatch` não estiver definido, o servidor usará os atributos do catálogo correspondente. Neste caso, `*`rootId`*` foi substituído por `attribute::RootPath` (ou `default::RootPath`, se não estiver especificado neste catálogo).

Se `attribute::FullMatch` estiver definido, o servidor ignorará completamente o catálogo, como se nenhum catálogo tivesse sido correspondido, e continuará usando os atributos de catálogo padrão. Nesse caso, `*`rootId`*` permanece parte do caminho (que é precedido por `default::RootPath`).

## Propriedades {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Sinalizador. Defina como 0 para comportamento padrão ou como 1 para ativar o comportamento de correspondência total.

## Padrão {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Herdado de `default::FullMatch` se não estiver definido ou se estiver vazio.

## Consulte também {#section-42da0ba53e0b4c089c62108785faf5a9}

[attribute::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
