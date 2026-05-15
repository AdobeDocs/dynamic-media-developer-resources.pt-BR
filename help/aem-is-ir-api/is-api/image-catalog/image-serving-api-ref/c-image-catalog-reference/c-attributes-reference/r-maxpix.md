---
description: Limite de tamanho da imagem de resposta. Largura e altura máximas da imagem de resposta que podem ser retornadas ao cliente.
solution: Experience Manager
title: MaxPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0fd990cf-a54f-4574-8328-8988368d5875
TQID: 'https://experienceleague.adobe.com/lX4ooC7B0VIJDRr0yZJVmp45qnXbSuimMZSyU9rWLcw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 0%

---

# MaxPix{#maxpix}

Limite de tamanho da imagem de resposta. Largura e altura máximas da imagem de resposta que podem ser retornadas ao cliente.

O servidor retornará um erro se uma solicitação fizer com que uma imagem de resposta com largura ou altura maior que `attribute::MaxPix`.

## Propriedades {#section-b175425b9e9f48e0b1a71640f6a9e936}

Dois números inteiros, maiores que 0, separados por vírgula. Largura e altura em pixels. Também pode ser definido como `0,0` para permitir qualquer tamanho de imagem de resposta sem limitações.

## Padrão {#section-1003537434da432fb2af100ecdbf9d72}

Herdado de `default::MaxPix` se não estiver definido ou se estiver vazio.

## Consulte também {#section-7385697a1b86482bba19db894f7af95b}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)
