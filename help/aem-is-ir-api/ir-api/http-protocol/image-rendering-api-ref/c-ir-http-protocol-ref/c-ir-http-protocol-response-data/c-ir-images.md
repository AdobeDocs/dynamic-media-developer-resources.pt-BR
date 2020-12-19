---
description: Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req= tiver um dos valores a seguir img, debug
seo-description: Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req= tiver um dos valores a seguir img, debug
seo-title: Imagens
solution: Experience Manager
title: Imagens
topic: Scene7 Image Serving - Image Rendering API
uuid: 8e8c5ec9-dc15-4894-b6a1-8e5241f03977
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# Imagens{#images}

Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req= tiver um dos seguintes valores: img, debug

O tipo MIME de resposta HTTP é determinado por `fmt=` ou, se `fmt=` não for especificado, depende do valor de `attribute::Format`.

O status da resposta HTTP será &#39;200 OK&#39; se o método de solicitação for incondicional `GET` ou `HEAD`.

O servidor pode responder com o status &#39;304&#39; (não modificado) e não retornar nenhum dado de imagem em resposta a uma solicitação condicional `GET` (com o campo [!DNL If-Modified-Since] presente em `request-header`).
