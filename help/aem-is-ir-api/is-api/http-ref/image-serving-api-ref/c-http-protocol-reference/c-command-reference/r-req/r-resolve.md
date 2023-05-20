---
description: Solicitação de depuração. Esse comando debug analisa e pré-processa a solicitação, executa pesquisas de catálogo de imagens, inclusões de modificador de catálogo, substituições de macro e variável etc., exatamente como req=img.
solution: Experience Manager
title: resolver
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---

# resolver{#resolve}

Solicitação de depuração. Esse comando debug analisa e pré-processa a solicitação, executa pesquisas no catálogo de imagens, catalog::Inclusões de modificadores, substituições de macro e variável etc., exatamente como req=img.

`req=resolve`

A string de solicitação final é retornada, em vez da imagem resultante, com o tipo MIME `text/plain`.

A resposta HTTP não pode ser armazenada em cache.
