---
description: Máscara de imagem. Solicita os dados da máscara (canal alfa).
seo-description: Máscara de imagem. Solicita os dados da máscara (canal alfa).
seo-title: máscara
solution: Experience Manager
title: máscara
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a8dc4bc-0757-45d2-adfe-d4bd69b4efa9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# máscara{#mask}

Máscara de imagem. Solicita os dados da máscara (canal alfa).

`req=mask`

Suporta os mesmos comandos `req=img`e é processado da mesma forma pelo servidor, mas em vez de retornar os dados RGB ou RGBA, o servidor descarta as informações de cores e retorna somente os dados de máscara (canal alfa). O formato de dados de resposta e o tipo MIME de resposta são determinados por `fmt=`.

A resposta HTTP pode ser armazenada em cache com o TTL baseado em `catalog::Expiration`.
