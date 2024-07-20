---
description: Se req=img, o tamanho da tela de composição é determinado inteiramente pelo tamanho da camada 0.
solution: Experience Manager
title: A tela de composição
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 38b2349f-714a-4304-bd33-5ce171b6d3a1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# A tela de composição{#the-compositing-canvas}

Se req=img, o tamanho da tela de composição é determinado inteiramente pelo tamanho da camada 0.

Se o `size=` da camada 0 não for especificado explicitamente, as transformações de camada serão usadas para calcular o tamanho da tela de composição (veja abaixo).

Se `req=tmb`, o tamanho da tela de composição será determinado pela `size=` especificada para a camada 0 ou, se o tamanho não for especificado, a tela de composição será definida como o tamanho de exibição correta (veja abaixo).
