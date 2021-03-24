---
description: Máscara de imagem. Solicita os dados da máscara (canal alfa).
solution: Experience Manager
title: máscara
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: ddfccb4ca157764e39fc719d96b63e6ee95304bf
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# máscara{#mask}

Máscara de imagem. Solicita os dados da máscara (canal alfa).

`req=mask`

Suporta os mesmos comandos que `req=img`. Ele é processado da mesma forma pelo servidor, mas em vez de retornar os dados RGB ou RGBA, o servidor descarta as informações de cor e retorna somente os dados de máscara (canal alfa). O formato dos dados de resposta e o tipo MIME de resposta são determinados por `fmt=`.

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::Expiration`.
