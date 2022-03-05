---
title: Materiais de coloração
description: A maioria dos materiais pode ser colorida dinamicamente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# Materiais de coloração{#colorizing-materials}

A maioria dos materiais pode ser colorida dinamicamente.

O algoritmo de colorização é simplista e funciona melhor para imagens materiais que têm um intervalo de matiz limitado. Para colorir um material, o renderizador simplesmente subtrai o `bgc=` e adiciona a variável `color=` para cada valor de pixel.

A colorização estará desativada se `color=` não especificado. O `bgc=` for ignorado pelos materiais do gabinete; o valor de cor base incorporado na [!DNL vnc] em vez disso, o arquivo é usado.
