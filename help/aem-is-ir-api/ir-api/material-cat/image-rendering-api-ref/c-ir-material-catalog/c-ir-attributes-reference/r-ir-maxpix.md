---
description: Limite de tamanho da imagem de resposta. Largura e altura máximas da imagem de resposta que podem ser retornadas ao cliente.
seo-description: Limite de tamanho da imagem de resposta. Largura e altura máximas da imagem de resposta que podem ser retornadas ao cliente.
seo-title: MaxPix
solution: Experience Manager
title: MaxPix
uuid: 8fc5e032-cfbb-40b5-9c3a-a2ec1bc4c3e2
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# MaxPix{#maxpix}

Limite de tamanho da imagem de resposta. Largura e altura máximas da imagem de resposta que podem ser retornadas ao cliente.

O servidor retornará um erro se uma solicitação causar uma imagem de resposta cuja largura e/ou altura for maior que `attribute::MaxSize`.

## Propriedades {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

Dois números inteiros, maiores que 0, separados por vírgula. Largura e altura em pixels. Também pode ser definido como 0,0 para permitir qualquer tamanho de imagem de resposta sem limitações.

## Padrão {#section-45b38dc661854d11b97df5709f4f3434}

Herdado do padrão::MaxPix se não estiver definido ou se estiver vazio.

## Consulte também {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) ,  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)
