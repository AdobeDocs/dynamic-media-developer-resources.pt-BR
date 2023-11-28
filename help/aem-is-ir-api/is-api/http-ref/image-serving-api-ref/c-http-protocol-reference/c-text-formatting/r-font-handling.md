---
title: Manuseio de fonte
description: Todas as fontes referenciadas na cadeia de caracteres RTF devem estar disponíveis no arquivo de mapa de fontes do catálogo padrão ou do catálogo de imagens atual, caso contrário, um erro será retornado.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e8e3ce9850ab8059aed81e720574d0c93f867a22
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 0%

---

# Manuseio de fonte{#font-handling}

Todas as fontes referenciadas na cadeia de caracteres RTF devem estar disponíveis no arquivo de mapa de fontes do catálogo padrão ou do catálogo de imagens atual, caso contrário, um erro será retornado.

A melhor qualidade para o texto em itálico e negrito é alcançada pelo registro dos arquivos de fonte correspondentes. Se não estiver disponível, o servidor pode sintetizar faces de fonte em negrito e/ou itálico a partir da face padrão. (Consulte [attribute::SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

A face da fonte especificada com `attribute::DefaultFont` é usado quando nenhum é especificado explicitamente na cadeia de caracteres RTF.

O Servidor de imagens é compatível com fontes TrueType, OpenType®, Adobe Type 1 (somente Windows).

<!-- THIS APPEARS TO BE VERY OLD OUTDATED INFORMATION; URL IS DEAD TOO ## Photofont&reg; font support {#section-74560ae898cf4708aba4c8b4093f5f00}

Photofont&reg; fonts support `textPs=`, with the following restrictions:

* `\cf` is ignored in text spans that specify a Photofont font; Photofont font faces have predefined colors 
* Synthesized font styles are not supported; use of `\b` and `\i`require corresponding font map entries, otherwise an error is returned 

* Vertical text flow is not supported 
* Photofont fonts with 16-bit images are not supported 
* Photofont fonts with multiple glyphs per image are not supported 
* Naïve color conversion is applied unless the Photofont glyph images embed color profiles; in this case, relative colorimetric render intent and blackpoint compensation are always applied

See [https://www.photofont.com](https://www.photofont.com) for additional information. -->

## Consulte também {#section-6cb8a802aa044836bbe449d559093f3a}

[Referência do mapa de fontes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107)
