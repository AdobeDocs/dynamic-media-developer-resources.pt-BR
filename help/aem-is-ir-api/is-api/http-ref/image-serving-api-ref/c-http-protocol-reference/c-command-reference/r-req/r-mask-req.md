---
description: Máscara de imagem. Solicita os dados da máscara (canal alfa).
solution: Experience Manager
title: máscara
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 0e743fe5-a623-4f5f-bc61-536ed70532bf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# máscara{#mask}

Máscara de imagem. Solicita os dados da máscara (canal alfa).

`req=mask`

Suporta os mesmos comandos que `req=img`. Ele é processado da mesma forma pelo servidor, mas em vez de retornar os dados RGB ou RGBA, o servidor descarta as informações de cor e retorna somente os dados de máscara (canal alfa). O formato dos dados de resposta e o tipo MIME de resposta são determinados por `fmt=`.

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::Expiration`.
