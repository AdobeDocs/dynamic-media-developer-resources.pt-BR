---
description: Tamanho padrão da imagem de renderização. O servidor restringe as imagens de resposta a não serem maiores que essa largura e altura, se a solicitação não especificar o tamanho da visualização explicitamente usando wid= ou hei=.
seo-description: Tamanho padrão da imagem de renderização. O servidor restringe as imagens de resposta a não serem maiores que essa largura e altura, se a solicitação não especificar o tamanho da visualização explicitamente usando wid= ou hei=.
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 27574811-a920-4e54-8635-5a643b8655ef
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# DefaultPix{#defaultpix}

Tamanho padrão da imagem de renderização. O servidor restringe as imagens de resposta a não serem maiores que essa largura e altura, se a solicitação não especificar o tamanho da visualização explicitamente usando wid= ou hei=.

## Propriedades {#section-9dc5474fc75842308796ab6440b29611}

Dois números inteiros, 0 ou maior, separados por uma vírgula. Largura e altura em pixels. Um ou ambos os valores podem ser definidos como 0 para mantê-los sem restrições.

Não se aplica a solicitações aninhadas/incorporadas.

## Padrão {#section-1935781c561e4679aa87a5bcced8df90}

Herdado de `default::DefaultPix` se não estiver definido ou se estiver vazio.

## Consulte também {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [atributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
