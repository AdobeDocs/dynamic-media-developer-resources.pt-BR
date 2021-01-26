---
description: A maioria dos materiais pode ser colorida dinamicamente.
seo-description: A maioria dos materiais pode ser colorida dinamicamente.
seo-title: Materiais de coloração
solution: Experience Manager
title: Materiais de coloração
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Colorir materiais{#colorizing-materials}

A maioria dos materiais pode ser colorida dinamicamente.

O algoritmo de colorização é bastante simplista e funciona melhor para imagens materiais que têm um intervalo de matiz limitado. Para colorir um material, o renderizador simplesmente subtrai o valor `bgc=` e adiciona o valor `color=` a cada valor de pixel.

A colorização será desabilitada se `color=` não for especificado. `bgc=` for ignorada pelos materiais da caixa; em vez disso, é usado o valor de cor base incorporado no  [!DNL vnc] arquivo.
