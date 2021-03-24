---
description: Opção de correspondência do catálogo.
solution: Experience Manager
title: FullMatch
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---


# FullMatch{#fullmatch}

Opção de correspondência do catálogo.

Uma entrada de catálogo é especificada como um par `*`rootId`*/ *`imageId`*` em solicitações HTTP. Ao analisar, um catálogo será selecionado se `*`rootId`*` corresponder ao valor `attribute::RootId` do catálogo e o registro do catálogo for identificado pela correspondência `*`imageId`*` com um valor `catalog::Id`. Se um catálogo for encontrado, mas não houver uma entrada de catálogo correspondente a `*`imageId`*`, o servidor poderá fazer uma das duas coisas a seguir:

Se `attribute::FullMatch` não estiver definido, o servidor usará os atributos do catálogo correspondente. Nesse caso, `*`rootId`*` é substituído por `attribute::RootPath` (ou `default::RootPath`, se não especificado neste catálogo).

Se `attribute::FullMatch` for definido, o servidor ignorará completamente o catálogo, como se nenhum catálogo tivesse sido correspondido, e continuará usando os atributos padrão do catálogo. Nesse caso, `*`rootId`*` permanece parte do caminho (que é anexado por `default::RootPath`).

## Propriedades {#section-25e021dbe6574d00aadd08a7fa0b6e81}

Sinalizador. Defina como 0 para o comportamento padrão ou como 1 para ativar o comportamento de correspondência completa.

## Padrão {#section-01c9ea1f1f1d4fd3b5f92799ec8383ff}

Herdado de `default::FullMatch` se não estiver definido ou se estiver vazio.

## Consulte também {#section-42da0ba53e0b4c089c62108785faf5a9}

[atributo::RootId](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546) ,  [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
