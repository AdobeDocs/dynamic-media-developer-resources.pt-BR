---
title: Materiais para colorir
description: A maioria dos materiais pode ser colorizada dinamicamente.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95b13a57-f10b-4ff2-90fd-507e69cb2b04
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# Materiais para colorir{#colorizing-materials}

A maioria dos materiais pode ser colorizada dinamicamente.

O algoritmo de colorização é simplista e funciona melhor para imagens de material com uma gama limitada de matizes. Para colorir um material, o renderizador simplesmente subtrai o `bgc=` e adiciona o `color=` para cada valor de pixel.

A coloração é desativada se `color=` não foi especificado. A variável `bgc=` atributo é ignorado pelos materiais do gabinete; o valor da cor base incorporado no [!DNL vnc] arquivo é usado em seu lugar.
