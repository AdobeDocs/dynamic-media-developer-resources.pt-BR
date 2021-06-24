---
description: Seletor de marca d'água. Especifica a ID de catálogo do registro de catálogo a ser usado como imagem de marca d'água ou modelo.
solution: Experience Manager
title: Marca d'água
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# Marca d&#39;água{#watermark}

Seletor de marca d&#39;água. Especifica o catálogo::Id do registro do catálogo a ser usado como imagem de marca d&#39;água ou modelo.

Se especificado, o servidor aplica a marca d&#39;água aos dados de imagem solicitados para todas as solicitações de imagem ( `req=img`).

## Propriedades {#section-fad6ffff4c5f4b5c8010281bc1377055}

Sequência de texto. Se especificado, deve ser um valor `Catalog::Id` válido neste catálogo de imagens (ou no catálogo padrão, se especificado em [!DNL default.ini]).

## Padrão {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Herdado de `default::Watermark` se não estiver definido. Se definida, mas estiver vazia, nenhuma marca d&#39;água será aplicada para este catálogo de imagem, mesmo se `default::Watermark` estiver definido.

## Consulte também {#section-f15dbe31013849828d78588742dde58e}

[catálogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
