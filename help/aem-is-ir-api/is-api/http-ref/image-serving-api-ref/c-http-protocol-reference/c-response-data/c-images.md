---
description: Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req=img ou req=tmb.
seo-description: Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req=img ou req=tmb.
seo-title: Imagens
solution: Experience Manager
title: Imagens
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# Imagens{#images}

Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req=img ou req=tmb.

O tipo MIME da resposta HTTP é determinado por `fmt=` ou, se `fmt=` não for especificado, será `<image/jpeg>`.

O status da resposta HTTP será &#39;200 OK&#39; se o método de solicitação for incondicional `GET` ou `HEAD`.

O servidor pode responder com o status &#39;304&#39; (não modificado) e não retornar nenhum dado de imagem em resposta a uma solicitação condicional `GET` (que inclui um cabeçalho válido `If-Modified-Since` ou `If-None-Match`).
