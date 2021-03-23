---
description: A renderização de imagem aplica materiais a grupos ou objetos em vinhetas.
seo-description: A renderização de imagem aplica materiais a grupos ou objetos em vinhetas.
seo-title: Materiais
solution: Experience Manager
title: Materiais
uuid: 82284e25-cfe0-4cf8-b410-b49196cc721c
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# Materiais{#materials}

A renderização de imagem aplica materiais a grupos ou objetos em vinhetas.

Um material consiste em um conjunto de *attributes*. Alguns atributos são necessários para determinados materiais, outros são opcionais e alguns são ignorados se estiverem presentes. Muitos atributos têm valores padrão. Nem todos os materiais podem ser aplicados a todos os objetos (por exemplo, um material de gabinete não pode ser aplicado a um sofá).

Quaisquer atributos que ocorram em um Segmento de especificação de material (MSS), mas não estejam listados acima nem nas tabelas de materiais específicas abaixo, são ignorados pelo servidor.

As tabelas a seguir listam os atributos básicos de material. O IR suporta atributos adicionais para controlar [efeitos de renderização avançados](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

Salvo indicação em contrário, todos os atributos de material são opcionais, com valores padrão adequados.

* [Cores sólidas](r-ir-solid-colors.md)
* [Texturas repetidas](r-ir-repeatable-textures.md)
* [Bordas de mural](r-ir-wall-borders.md)
* [Decretos](r-ir-decals.md)
* [Gabinetes](r-ir-cabinets.md)
* [Coberturas de janelas](r-ir-window-coverings.md)
