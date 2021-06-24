---
description: Pré-carregar o cache do servidor. Executa a solicitação exatamente como req=img, mas em vez de retornar a imagem, o servidor retorna o comprimento da imagem de resposta (image.length), formatada como dados de texto com texto/sem formatação do tipo MIME.
solution: Experience Manager
title: loadcache
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 653842e9-bed1-462a-bb1f-39ac1ac9512c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 0%

---

# loadcache{#loadcache}

Pré-carregar o cache do servidor. Executa a solicitação exatamente como req=img, mas em vez de retornar a imagem, o servidor retorna o comprimento da imagem de resposta (image.length), formatada como dados de texto com texto/sem formatação do tipo MIME.

`req=loadcache`

A resposta HTTP não pode ser armazenada em cache.

Outros comandos na solicitação se aplicam conforme documentado.
