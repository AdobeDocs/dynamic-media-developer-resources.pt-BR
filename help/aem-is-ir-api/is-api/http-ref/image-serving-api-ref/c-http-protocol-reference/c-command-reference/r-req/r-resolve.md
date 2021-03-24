---
description: Solicitação de depuração. Este comando de depuração analisa e pré-processa a solicitação, executa pesquisas de catálogo de imagem, inclusões de modificador de catálogo, substituições de macro e variável, etc, exatamente como req=img.
solution: Experience Manager
title: resolve
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 0%

---


# resolve{#resolve}

Solicitação de depuração. Este comando de depuração analisa e pré-processa a solicitação, executa pesquisas de catálogo de imagem, catálogo::Inclusões de modificador, substituições de macro e variável, etc, exatamente como req=img.

`req=resolve`

A cadeia de caracteres de solicitação final é retornada, em vez da imagem de resultado, com o tipo MIME `text/plain`.

A resposta HTTP não pode ser armazenada em cache.
