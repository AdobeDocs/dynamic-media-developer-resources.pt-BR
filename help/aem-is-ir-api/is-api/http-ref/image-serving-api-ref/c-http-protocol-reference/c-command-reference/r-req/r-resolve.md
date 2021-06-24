---
description: Solicitação de depuração. Este comando de depuração analisa e pré-processa a solicitação, executa pesquisas de catálogo de imagem, inclusões de modificador de catálogo, substituições de macro e variável, etc, exatamente como req=img.
solution: Experience Manager
title: resolve
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: ef357c19-e725-4904-b635-102e75ff7518
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 0%

---

# resolve{#resolve}

Solicitação de depuração. Este comando de depuração analisa e pré-processa a solicitação, executa pesquisas de catálogo de imagem, catálogo::Inclusões de modificador, substituições de macro e variável, etc, exatamente como req=img.

`req=resolve`

A cadeia de caracteres de solicitação final é retornada, em vez da imagem de resultado, com o tipo MIME `text/plain`.

A resposta HTTP não pode ser armazenada em cache.
