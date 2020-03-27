---
description: A maioria dos materiais pode ser colorida dinamicamente.
seo-description: A maioria dos materiais pode ser colorida dinamicamente.
seo-title: Materiais de coloração
solution: Experience Manager
title: Materiais de coloração
topic: Scene7 Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Materiais de coloração{#colorizing-materials}

A maioria dos materiais pode ser colorida dinamicamente.

O algoritmo de colorização é bastante simplista e funciona melhor para imagens materiais que têm um intervalo de matiz limitado. Para colorir um material, o renderizador simplesmente subtrai o `bgc=` valor e adiciona o `color=` valor a cada valor de pixel.

A colorização será desativada se não `color=` for especificada. `bgc=` for ignorada pelos materiais da caixa; em vez disso, é usado o valor de cor base incorporado no [!DNL vnc] arquivo.
