---
description: Seletor de mapa de iluminação. Especifica o mapa de iluminação com o qual este material prefere ser renderizado.
solution: Experience Manager
title: íleo
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# illum{#illum}

Seletor de mapa de iluminação. Especifica o mapa de iluminação com o qual este material prefere ser renderizado.

`illum=-1|0|1|2`

Se o mapa de iluminação especificado não estiver disponível na vinheta-alvo, é utilizado o mapa disponível mais próximo.

`illum=-1` especifica que o mapa de iluminação é selecionado automaticamente com base no  `gloss=` valor.

## Propriedades {#section-aace8466566e4cf1a0c5a6c0167245c9}

Atributo de material. Ignorado se a vinheta não definir mapas de iluminação múltiplos.

## Padrão {#section-c96ecfb232074e80b6a29076f5199403}

`illum=-1`

## Consulte também {#section-9132e60381c64aa3a8ed1319690db55e}

[brilho=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca)
