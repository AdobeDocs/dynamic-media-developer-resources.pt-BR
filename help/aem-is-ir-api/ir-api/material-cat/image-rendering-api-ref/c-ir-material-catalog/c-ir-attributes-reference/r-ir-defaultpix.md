---
title: DefaultPix
description: Tamanho de imagem de renderização padrão. As restrições do servidor respondem que as imagens não são maiores que essa largura e altura se a solicitação não especificar explicitamente o tamanho da exibição usando wid= ou hei=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d60f2b8c-5213-42ad-8ec9-7e7797d74e09
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# DefaultPix{#defaultpix}

Tamanho de imagem de renderização padrão. As restrições do servidor respondem que as imagens não são maiores que essa largura e altura se a solicitação não especificar explicitamente o tamanho da exibição usando wid= ou hei=.

## Propriedades {#section-9dc5474fc75842308796ab6440b29611}

Dois números inteiros, 0 ou maiores, separados por vírgula. Largura e altura em pixels. Um ou ambos os valores podem ser definidos como 0 para mantê-los sem restrições.

Não aplicável a solicitações aninhadas/incorporadas.

## Padrão {#section-1935781c561e4679aa87a5bcced8df90}

Herdado de `default::DefaultPix` se não estiver definido ou se estiver vazio.

## Consulte também {#section-d28f18d29ef14692b8706ca08e754f54}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attribute::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657)
