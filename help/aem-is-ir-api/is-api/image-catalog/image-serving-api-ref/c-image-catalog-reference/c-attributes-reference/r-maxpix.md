---
description: Limite de tamanho da imagem de resposta. Largura e altura máximas da imagem de resposta que podem ser retornadas ao cliente.
seo-description: Limite de tamanho da imagem de resposta. Largura e altura máximas da imagem de resposta que podem ser retornadas ao cliente.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
topic: Scene7 Image Serving - Image Rendering API
uuid: 22c5fac8-1e64-4917-8bb8-69a95ab549cb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---


# MaxPix{#maxpix}

Limite de tamanho da imagem de resposta. Largura e altura máximas da imagem de resposta que podem ser retornadas ao cliente.

O servidor retornará um erro se uma solicitação causar uma imagem de resposta cuja largura ou altura seja maior que `attribute::MaxPix`.

## Propriedades {#section-b175425b9e9f48e0b1a71640f6a9e936}

Dois números inteiros, maiores que 0, separados por uma vírgula. Largura e altura em pixels. Também pode ser definido como `0,0` para permitir qualquer tamanho de imagem de resposta sem limitações.

## Padrão {#section-1003537434da432fb2af100ecdbf9d72}

Herdado de `default::MaxPix` se não estiver definido ou se estiver vazio.

## Consulte também {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
