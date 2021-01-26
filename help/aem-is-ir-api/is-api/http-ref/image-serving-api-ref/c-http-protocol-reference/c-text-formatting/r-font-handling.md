---
description: Todas as fontes referenciadas na string RTF devem estar disponíveis no arquivo de mapa de fontes do catálogo padrão ou no catálogo de imagens atual, caso contrário um erro será retornado.
seo-description: Todas as fontes referenciadas na string RTF devem estar disponíveis no arquivo de mapa de fontes do catálogo padrão ou no catálogo de imagens atual, caso contrário um erro será retornado.
seo-title: Manuseio de fonte
solution: Experience Manager
title: Manuseio de fonte
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6a751973-5dae-472e-a908-bf24fa59d031
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---


# Manuseio de fonte{#font-handling}

Todas as fontes referenciadas na string RTF devem estar disponíveis no arquivo de mapa de fontes do catálogo padrão ou no catálogo de imagens atual, caso contrário um erro será retornado.

A melhor qualidade para textos em itálico e em negrito é alcançada pelo registro dos arquivos de fonte correspondentes. Se não estiver disponível, o servidor poderá sintetizar faces de fonte em negrito e/ou itálico a partir da face padrão. (Consulte ` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`.)

A face de fonte especificada com `attribute::DefaultFont` é usada quando nenhum é especificado explicitamente na string RTF.

O Serviço de imagem oferece suporte a fontes TrueType, OpenType, Adobe Type 1 (somente Windows).

## Suporte a fontes do Photofont® {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` suporta fontes Photofont®, com as seguintes restrições:

* `\cf` é ignorada em extensões de texto que especificam uma fonte Photofont; As faces de fontes de fontes fotográficas têm cores predefinidas
* Não há suporte para estilos de fonte sintetizados; o uso de `\b` e `\i`exigem entradas correspondentes do mapa de fontes, caso contrário, um erro será retornado

* O fluxo de texto vertical não é suportado
* Fontes de fontes fotográficas com imagens de 16 bits não são compatíveis
* Fontes de fontes fotográficas com vários glifos por imagem não são suportadas
* A conversão de cores ingênua é aplicada, a menos que as imagens de glifo de Photofont incorporem perfis coloridos; nesse caso, a intenção de renderização colorimétrica relativa e a compensação do ponto de negação são sempre aplicadas

Consulte ` [www.photofont.com](http://www.photofont.com)` para obter mais informações.

## Consulte também {#section-6cb8a802aa044836bbe449d559093f3a}

[Referência](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d) do mapa de fontes,  [atributo::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15),  [atributo::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107),  [ [!DNL www.photofont.com] ](http://www.photofont.com)
