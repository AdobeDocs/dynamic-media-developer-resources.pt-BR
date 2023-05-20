---
title: Manuseio de fonte
description: Todas as fontes referenciadas na cadeia de caracteres RTF devem estar disponíveis no arquivo de mapa de fontes do catálogo padrão ou do catálogo de imagens atual, caso contrário, um erro será retornado.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f24edd53-4b21-4147-9b50-95e616279aa8
source-git-commit: e1f0f8bdac2b7a8397adac3bb9ba38d0c519f8fb
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# Manuseio de fonte{#font-handling}

Todas as fontes referenciadas na cadeia de caracteres RTF devem estar disponíveis no arquivo de mapa de fontes do catálogo padrão ou do catálogo de imagens atual, caso contrário, um erro será retornado.

A melhor qualidade para o texto em itálico e negrito é alcançada pelo registro dos arquivos de fonte correspondentes. Se não estiver disponível, o servidor pode sintetizar faces de fonte em negrito e/ou itálico a partir da face padrão. (Consulte [attribute::SynthesizeFontStyles](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md).

A face da fonte especificada com `attribute::DefaultFont` é usado quando nenhum é especificado explicitamente na cadeia de caracteres RTF.

O Servidor de imagens é compatível com fontes TrueType, OpenType, Adobe Type 1 (somente Windows).

## Suporte a fontes Photofont® {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` O suporta fontes Photofont®, com as seguintes restrições:

* `\cf` é ignorada em extensões de texto que especificam uma fonte &#39;Photofont&#39;; faces &#39;Photofont&#39; possuem cores predefinidas
* Estilos de fonte sintetizados não são suportados; uso de `\b` e `\i`exigir entradas de mapa de fontes correspondentes; caso contrário, um erro será retornado

* Não há suporte para fluxo de texto vertical
* Fontes Photofont com imagens de 16 bits não são suportadas
* Fontes de fontes fototipo com vários glifos por imagem não são suportadas
* A conversão de cores ingênuas é aplicada a menos que as imagens de glifo de fontes fotográficas integrem perfis de cores; nesse caso, a intenção de renderização colorimétrica relativa e a compensação de pontos negros são sempre aplicadas

Consulte [www.photofont.com](https://www.photofont.com) para obter informações adicionais.

## Consulte também {#section-6cb8a802aa044836bbe449d559093f3a}

[Referência do mapa de fontes](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d), [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15), [attribute::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107), [ [!DNL www.photofont.com] ](https://www.photofont.com)
