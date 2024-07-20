---
title: resolver
description: Solicitação de depuração. Esse comando debug analisa e pré-processa a solicitação, executa pesquisas de catálogo de imagens, inclusões de modificador de catálogo, substituições de macro e variável, etc., exatamente como req=img.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# resolver{#resolve}

Solicitação de depuração. Esse comando debug analisa e pré-processa a solicitação, executa pesquisas de catálogo de imagens, catalog::Inclusões de modificadores, substituições de macro e variável, etc., exatamente como req=img.

`req=resolve`

A cadeia de caracteres de solicitação final é retornada, em vez da imagem resultante, com o tipo MIME `text/plain`.

A resposta HTTP não pode ser armazenada em cache.
