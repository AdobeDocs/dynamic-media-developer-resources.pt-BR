---
description: A maioria dos materiais pode ser colorida dinamicamente.
seo-description: A maioria dos materiais pode ser colorida dinamicamente.
seo-title: Materiais de coloração
solution: Experience Manager
title: Materiais de coloração
uuid: 3f5a9089-6e35-446c-89f9-71b067e0d1df
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---


# Colorir materiais{#colorizing-materials}

A maioria dos materiais pode ser colorida dinamicamente.

O algoritmo de coloração é bastante simplista e funciona melhor para imagens materiais que têm um intervalo de matiz limitado. Para colorir um material, o renderizador simplesmente subtrai o valor `bgc=` e adiciona o valor `color=` a cada valor de pixel.

A colorização será desabilitada se `color=` não for especificado. `bgc=` for ignorada por materiais de armário; em vez disso, o valor de cor base incorporado no  [!DNL vnc] arquivo é usado.
