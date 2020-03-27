---
description: Seletor de marca d'água. Especifica a ID de catálogo do registro de catálogo a ser usado como imagem de marca d'água ou modelo.
seo-description: Seletor de marca d'água. Especifica a ID de catálogo do registro de catálogo a ser usado como imagem de marca d'água ou modelo.
seo-title: Marca d'água
solution: Experience Manager
title: Marca d'água
topic: Scene7 Image Serving - Image Rendering API
uuid: 18add7ab-0797-4ab3-a7e8-05c745abe605
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# Marca d&#39;água{#watermark}

Seletor de marca d&#39;água. Especifica o catálogo::Id do registro do catálogo a ser usado como imagem de marca d&#39;água ou modelo.

Se especificado, o servidor aplica a marca d&#39;água aos dados de imagem solicitados para todas as solicitações de imagem ( `req=img`).

## Propriedades {#section-fad6ffff4c5f4b5c8010281bc1377055}

Sequência de caracteres de texto. Se especificado, deve ser um `Catalog::Id` valor válido neste catálogo de imagens (ou no catálogo padrão, se especificado em [!DNL default.ini]).

## Padrão {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Herdado de `default::Watermark` se não estiver definido. Se definido, mas vazio, nenhuma marca d&#39;água será aplicada a esse catálogo de imagens, mesmo se `default::Watermark` estiver definido.

## Consulte também {#section-f15dbe31013849828d78588742dde58e}

[catálogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
