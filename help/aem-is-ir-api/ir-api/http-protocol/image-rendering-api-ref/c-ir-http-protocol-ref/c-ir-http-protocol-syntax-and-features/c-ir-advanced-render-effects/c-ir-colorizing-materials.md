---
description: A maioria dos materiais pode ser colorida dinamicamente.
solution: Experience Manager
title: Materiais de coloração
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 0%

---

# Materiais de coloração{#colorizing-materials}

A maioria dos materiais pode ser colorida dinamicamente.

O algoritmo de coloração é bastante simplista e funciona melhor para imagens materiais que têm um intervalo de matiz limitado. Para colorir um material, o renderizador simplesmente subtrai o valor `bgc=` e adiciona o valor `color=` a cada valor de pixel.

A colorização será desabilitada se `color=` não for especificado. `bgc=` for ignorada por materiais de armário; em vez disso, o valor de cor base incorporado no  [!DNL vnc] arquivo é usado.
