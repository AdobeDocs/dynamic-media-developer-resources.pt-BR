---
description: Se req=img, o tamanho da tela de composição é determinado inteiramente pelo tamanho da camada 0.
solution: Experience Manager
title: A tela de composição
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 0%

---


# A tela de composição{#the-compositing-canvas}

Se req=img, o tamanho da tela de composição é determinado inteiramente pelo tamanho da camada 0.

Se `size=` para a camada 0 não for especificado explicitamente, as transformações de camada serão usadas para calcular o tamanho da tela de composição (veja abaixo).

Se `req=tmb`, o tamanho da tela de composição é determinado pelo `size=` especificado para a camada 0 ou, se o tamanho não for especificado, o tamanho da tela de composição é definido para o retângulo de exibição (veja abaixo).
