---
description: Seletor de mapa de iluminação. Especifica o mapa de iluminação que este material prefere ser renderizado.
seo-description: Seletor de mapa de iluminação. Especifica o mapa de iluminação que este material prefere ser renderizado.
seo-title: íleo
solution: Experience Manager
title: íleo
topic: Scene7 Image Serving - Image Rendering API
uuid: 16c7144f-7f16-47d1-8140-fd679e702660
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# íleo{#illum}

Seletor de mapa de iluminação. Especifica o mapa de iluminação que este material prefere ser renderizado.

`illum=-1|0|1|2`

Se o mapa de iluminação especificado não estiver disponível na vinheta de público alvo, é utilizado o mapa disponível mais próximo.

`illum=-1` especifica que o mapa de iluminação é selecionado automaticamente com base no `gloss=` valor.

## Propriedades {#section-aace8466566e4cf1a0c5a6c0167245c9}

Atributo material. Ignorado se a vinheta não definir mapas de iluminação múltiplos.

## Padrão {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Consulte também {#section-9132e60381c64aa3a8ed1319690db55e}

[brilho=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
