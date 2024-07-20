---
description: Seletor de marca d'água. Especifica a Id do catálogo do registro de catálogo a ser usado como uma imagem de marca d'água ou modelo.
solution: Experience Manager
title: Marca d'água
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54c27ea0-e87f-41ce-ae8d-71c9fabe412e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---

# Marca d&#39;água{#watermark}

Seletor de marca d&#39;água. Especifica o catálogo::Id do registro de catálogo a ser usado como imagem de marca d&#39;água ou modelo.

Se especificado, o servidor aplica a marca d&#39;água aos dados de imagem solicitados para todas as solicitações de imagem ( `req=img`).

## Propriedades {#section-fad6ffff4c5f4b5c8010281bc1377055}

String de texto. Se especificado, deve ser um valor `Catalog::Id` válido neste catálogo de imagens (ou no catálogo padrão, se especificado em [!DNL default.ini]).

## Padrão {#section-f8a2029b5b8740b2af149bdbfa28fbae}

Herdado de `default::Watermark` se não estiver definido. Se definido, mas vazio, nenhuma marca d&#39;água é aplicada a este catálogo de imagens, mesmo se `default::Watermark` for definido.

## Consulte também {#section-f15dbe31013849828d78588742dde58e}

[catálogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md)
