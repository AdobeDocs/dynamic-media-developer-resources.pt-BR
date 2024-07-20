---
title: Materiais
description: A Renderização de imagem aplica materiais a grupos ou objetos em vinhetas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Materiais{#materials}

A Renderização de imagem aplica materiais a grupos ou objetos em vinhetas.

Um material consiste em um conjunto de *atributos*. Alguns atributos são necessários para certos materiais, outros são opcionais e alguns são ignorados se estiverem presentes. Muitos atributos têm valores padrão. Nem todos os materiais podem ser aplicados a todos os objetos (por exemplo, um material de gabinete não pode ser aplicado a um sofá).

Quaisquer atributos que ocorrem dentro de um Segmento de Especificação de Material (MSS), mas que não estão listados acima ou nas tabelas de material específicas abaixo, são ignorados pelo servidor.

As tabelas a seguir listam os atributos básicos do material. O IR dá suporte a atributos adicionais para controlar [efeitos de renderização avançados](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Salvo indicação em contrário, todos os atributos de material são opcionais, com valores-padrão adequados.

* [Cores sólidas](r-ir-solid-colors.md)
* [Texturas repetíveis](r-ir-repeatable-textures.md)
* [Bordas da parede](r-ir-wall-borders.md)
* [Decalques](r-ir-decals.md)
* [Gabinetes](r-ir-cabinets.md)
* [Coberturas de janelas](r-ir-window-coverings.md)
