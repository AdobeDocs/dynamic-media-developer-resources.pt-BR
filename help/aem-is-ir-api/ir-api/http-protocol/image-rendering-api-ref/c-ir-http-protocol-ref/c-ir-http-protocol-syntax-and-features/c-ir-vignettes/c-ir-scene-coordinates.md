---
description: O espaço de coordenadas da cena é usado para especificar tamanhos de e distâncias nas superfícies do objeto textualizável.
solution: Experience Manager
title: Coordenadas da cena
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: de7f088e-3825-4d2e-924e-001a44db62a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# Coordenadas da cena{#scene-coordinates}

O espaço de coordenadas da cena é usado para especificar tamanhos de e distâncias nas superfícies do objeto textualizável.

Como a maioria das vinhetas são cenas do mundo real representando objetos físicos, a maioria das vinhetas é criada usando polegadas como unidades para o espaço de coordenadas da cena. Podem também ser utilizadas outras unidades, como mm ou cm. A Renderização de Imagem não suporta a conversão de unidade.

Os seguintes comandos aceitam valores no espaço de coordenadas de cena:

* [grout=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a)
* [pos=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8)
* [size=](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988)
