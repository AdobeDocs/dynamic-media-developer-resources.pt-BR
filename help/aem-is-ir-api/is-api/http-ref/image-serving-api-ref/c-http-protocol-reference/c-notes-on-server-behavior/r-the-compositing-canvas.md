---
description: Se req=img, o tamanho da tela de composição é determinado inteiramente pelo tamanho da camada 0.
solution: Experience Manager
title: A tela de composição
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---

# A tela de composição{#the-compositing-canvas}

Se req=img, o tamanho da tela de composição é determinado inteiramente pelo tamanho da camada 0.

Se `size=` para a camada 0 não for especificado explicitamente, as transformações de camada serão usadas para calcular o tamanho da tela de composição (veja abaixo).

Se `req=tmb`, o tamanho da tela de composição é determinado pelo `size=` especificado para a camada 0 ou, se o tamanho não for especificado, o tamanho da tela de composição é definido para o retângulo de exibição (veja abaixo).
