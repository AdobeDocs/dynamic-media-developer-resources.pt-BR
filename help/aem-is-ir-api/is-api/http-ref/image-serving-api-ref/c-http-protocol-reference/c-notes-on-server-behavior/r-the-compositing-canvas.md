---
description: Se req=img, o tamanho da tela de composição é determinado inteiramente pelo tamanho da camada 0.
seo-description: Se req=img, o tamanho da tela de composição é determinado inteiramente pelo tamanho da camada 0.
seo-title: A tela de composição
solution: Experience Manager
title: A tela de composição
uuid: 7ec2f1b3-61fc-4bfe-96d2-a5946a238e74
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# A tela de composição{#the-compositing-canvas}

Se req=img, o tamanho da tela de composição é determinado inteiramente pelo tamanho da camada 0.

Se `size=` para a camada 0 não for especificado explicitamente, as transformações de camada serão usadas para calcular o tamanho da tela de composição (veja abaixo).

Se `req=tmb`, o tamanho da tela de composição é determinado pelo `size=` especificado para a camada 0 ou, se o tamanho não for especificado, o tamanho da tela de composição é definido para o retângulo de exibição (veja abaixo).
