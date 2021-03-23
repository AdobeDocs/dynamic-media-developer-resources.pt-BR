---
description: Máscara de imagem. Solicita os dados da máscara (canal alfa).
seo-description: Máscara de imagem. Solicita os dados da máscara (canal alfa).
seo-title: máscara
solution: Experience Manager
title: máscara
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---


# máscara{#mask}

Máscara de imagem. Solicita os dados da máscara (canal alfa).

`req=mask`

Suporta os mesmos comandos que `req=img` e é processado da mesma forma pelo servidor, mas em vez de retornar os dados RGB ou RGBA, o servidor descarta as informações de cor e retorna somente os dados de máscara (canal alfa). O formato dos dados de resposta e o tipo MIME de resposta são determinados por `fmt=`.

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::Expiration`.
