---
description: Todas as fontes referenciadas na string RTF devem estar disponíveis no arquivo de mapa de fontes do catálogo padrão ou no catálogo de imagens atual; caso contrário, um erro será retornado.
seo-description: Todas as fontes referenciadas na string RTF devem estar disponíveis no arquivo de mapa de fontes do catálogo padrão ou no catálogo de imagens atual; caso contrário, um erro será retornado.
seo-title: Tratamento de fontes
solution: Experience Manager
title: Tratamento de fontes
uuid: 6a751973-5dae-472e-a908-bf24fa59d031
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 0%

---


# Manipulação de fonte{#font-handling}

Todas as fontes referenciadas na string RTF devem estar disponíveis no arquivo de mapa de fontes do catálogo padrão ou no catálogo de imagens atual; caso contrário, um erro será retornado.

A melhor qualidade para o texto em itálico e em negrito é alcançada pelo registro dos arquivos de fonte correspondentes. Se não estiver disponível, o servidor poderá sintetizar faces de fonte em negrito e/ou itálico a partir da face padrão. (Consulte ` [attribute::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15)`.)

A fonte especificada com `attribute::DefaultFont` é usada quando nenhuma é especificada explicitamente na string RTF.

O Image Serving suporta fontes TrueType, OpenType, Adobe Type 1 (somente Windows).

## Suporte a fontes do Photofont® {#section-74560ae898cf4708aba4c8b4093f5f00}

`textPs=` suporta fontes Photofont®, com as seguintes restrições:

* `\cf` é ignorado em extensões de texto que especificam uma fonte Photofont; Os rostos de fontes de fontes de fotos têm cores predefinidas
* Não há suporte para estilos de fonte sintetizados; o uso de `\b` e `\i`exigem entradas de mapa de fontes correspondentes, caso contrário, um erro é retornado

* O fluxo de texto vertical não é suportado
* Fontes de fontes fotográficas com imagens de 16 bits não são compatíveis
* Fontes de fontes fotográficas com vários glifos por imagem não são compatíveis
* A conversão de cores ingênua é aplicada, a menos que as imagens de glifo do Photofont incorporem perfis de cores; nesse caso, a intenção de renderização colorimétrica relativa e a compensação do ponto negro são sempre aplicadas

Consulte ` [www.photofont.com](http://www.photofont.com)` para obter mais informações.

## Consulte também {#section-6cb8a802aa044836bbe449d559093f3a}

[Referência](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-font-map-reference/c-font-map-reference.md#concept-f81f319d03c646c5a8ef87b3277dd37d) do mapa de fontes,  [atributo::SynthesizeFontStyles](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-synthesizefontstyles.md#reference-1b12ba881b9146c793bcb07407cacb15),  [atributo::DefaultFont](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultfont.md#reference-48b763ac254545e89a25c76ff7581107),  [ [!DNL www.photofont.com] ](http://www.photofont.com)
