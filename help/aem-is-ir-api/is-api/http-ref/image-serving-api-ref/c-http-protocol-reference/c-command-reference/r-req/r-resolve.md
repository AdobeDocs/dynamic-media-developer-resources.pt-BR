---
description: Solicitação de depuração. Esse comando de depuração analisa e pré-processa a solicitação, executa pesquisas no catálogo de imagens, inclusões no modificador de catálogo, substituições de macro e variável etc, exatamente como req=img.
seo-description: Solicitação de depuração. Esse comando de depuração analisa e pré-processa a solicitação, executa pesquisas no catálogo de imagens, inclusões no modificador de catálogo, substituições de macro e variável etc, exatamente como req=img.
seo-title: resolve
solution: Experience Manager
title: resolve
topic: Dynamic Media Image Serving - Image Rendering API
uuid: bd1576a7-4802-4a87-b1c0-406f51382561
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# resolve{#resolve}

Solicitação de depuração. Esse comando de depuração analisa e pré-processa a solicitação, executa pesquisas no catálogo de imagens, catálogo::Inclusões do modificador, substituições de macro e variável etc, da mesma forma que req=img.

`req=resolve`

A string de solicitação final é retornada, em vez da imagem resultante, com o tipo MIME `text/plain`.

A resposta HTTP não pode ser armazenada em cache.
