---
description: A maioria dos materiais pode ser colorida dinamicamente.
solution: Experience Manager
title: Materiais de coloração
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# Colorir materiais{#colorizing-materials}

A maioria dos materiais pode ser colorida dinamicamente.

O algoritmo de coloração é bastante simplista e funciona melhor para imagens materiais que têm um intervalo de matiz limitado. Para colorir um material, o renderizador simplesmente subtrai o valor `bgc=` e adiciona o valor `color=` a cada valor de pixel.

A colorização será desabilitada se `color=` não for especificado. `bgc=` for ignorada por materiais de armário; em vez disso, o valor de cor base incorporado no  [!DNL vnc] arquivo é usado.
