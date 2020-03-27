---
description: Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req=img ou req=tmb.
seo-description: Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req=img ou req=tmb.
seo-title: Imagens
solution: Experience Manager
title: Imagens
topic: Scene7 Image Serving - Image Rendering API
uuid: 715154b6-f9ac-459e-a566-f78a4ca4580d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Imagens{#images}

Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req=img ou req=tmb.

O tipo MIME de resposta HTTP é determinado por `fmt=`, ou, se não `fmt=` for especificado, é `<image/jpeg>`.

O status da resposta HTTP é &#39;200 OK&#39; se o método de solicitação for incondicional `GET` ou `HEAD`.

O servidor pode responder com o status &#39;304&#39; (não modificado) e não retornar nenhum dado de imagem em resposta a uma `GET` solicitação condicional (que inclui um cabeçalho válido `If-Modified-Since` ou `If-None-Match` ).
