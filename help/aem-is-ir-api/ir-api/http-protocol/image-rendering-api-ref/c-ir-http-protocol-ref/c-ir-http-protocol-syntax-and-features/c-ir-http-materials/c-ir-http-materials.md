---
description: A renderização de imagem aplica materiais a grupos ou objetos em vinhetas.
seo-description: A renderização de imagem aplica materiais a grupos ou objetos em vinhetas.
seo-title: Materiais
solution: Experience Manager
title: Materiais
topic: Scene7 Image Serving - Image Rendering API
uuid: 82284e25-cfe0-4cf8-b410-b49196cc721c
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Materiais{#materials}

A renderização de imagem aplica materiais a grupos ou objetos em vinhetas.

Um material consiste em um conjunto de *atributos*. Alguns atributos são obrigatórios para certos materiais, outros são opcionais e alguns são ignorados se presentes. Muitos atributos têm valores padrão. Nem todos os materiais podem ser aplicados a todos os objetos (por exemplo, um material de gabinete não pode ser aplicado a um sofá).

Todos os atributos que ocorrem em um Segmento de especificação de material (MSS), mas que não estão listados acima nem nas tabelas de material específicas abaixo, são ignorados pelo servidor.

As tabelas a seguir listas os atributos básicos de material. O IR suporta atributos adicionais para controlar [efeitos de renderização avançados](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Salvo indicação em contrário, todos os atributos de material são opcionais, com valores padrão adequados.

* [Cores sólidas](r-ir-solid-colors.md)
* [Texturas repetidas](r-ir-repeatable-textures.md)
* [Bordas de mural](r-ir-wall-borders.md)
* [Decretos](r-ir-decals.md)
* [Gabinetes](r-ir-cabinets.md)
* [Coberturas de janelas](r-ir-window-coverings.md)
