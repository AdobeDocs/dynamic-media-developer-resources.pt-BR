---
title: Materiais
description: A Renderização de imagem aplica materiais a grupos ou objetos em vinhetas.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
TQID: 'https://experienceleague.adobe.com/MNCMxRxVGLF2rsr7NsuTGLzWxM9zkR42MI9MLdaW6G8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
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
