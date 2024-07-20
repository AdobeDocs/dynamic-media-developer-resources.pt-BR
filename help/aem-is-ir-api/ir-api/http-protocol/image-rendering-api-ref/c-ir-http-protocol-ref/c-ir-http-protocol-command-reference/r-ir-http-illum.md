---
title: illum
description: Seletor de mapa de iluminação. Especifica o mapa de iluminação com o qual este material prefere ser renderizado.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e1af2397-8eae-4b77-abb1-61ba8cb866f3
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# illum{#illum}

Seletor de mapa de iluminação. Especifica o mapa de iluminação com o qual este material prefere ser renderizado.

`illum=-1|0|1|2`

Se o mapa de iluminação especificado não estiver disponível na vinheta de destino, será usado o mapa disponível mais próximo.

`illum=-1` Especifica que o mapa de iluminação é selecionado automaticamente com base no valor `gloss=`.

## Propriedades {#section-aace8466566e4cf1a0c5a6c0167245c9}

Atributo de material. Ignorado se a vinheta não definir vários mapas de iluminação.

## Padrão {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Consulte também {#section-9132e60381c64aa3a8ed1319690db55e}

[brilho=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
