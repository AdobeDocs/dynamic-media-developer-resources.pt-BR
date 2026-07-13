---
title: MaxPix
description: Limite de tamanho da imagem de resposta. Largura e altura máximas da imagem de resposta que podem ser retornadas ao cliente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48239519-7935-45e4-ae36-5e687a356cc1
TQID: 'https://experienceleague.adobe.com/pgrg9BCY7fJXGsoABNjMOwIhRxYzrmQpsDSyGd6GSCc'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 103
ht-degree: 0%

---

# MaxPix{#maxpix}

Limite de tamanho da imagem de resposta. Largura e altura máximas da imagem de resposta que podem ser retornadas ao cliente.

O servidor retorna um erro se uma solicitação causar uma imagem de resposta cuja largura e/ou altura é maior que `attribute::MaxSize`.

## Propriedades {#section-390c1066b7a748aca3c0b45ad8bdcfb1}

Dois números inteiros, maiores que 0, separados por vírgula. Largura e altura em pixels. Também pode ser definido como 0,0 para permitir qualquer tamanho de imagem de resposta sem limitações.

## Padrão {#section-45b38dc661854d11b97df5709f4f3434}

Herdado do padrão::MaxPix se não estiver definido ou se estiver vazio.

## Consulte também {#section-09cddedde91f43b1ac5828f7e3327c6a}

[wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec) , [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478)

