---
description: Os dados da imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req=img ou req=tmb.
solution: Experience Manager
title: Imagens
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 0%

---

# Imagens{#images}

Os dados da imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req=img ou req=tmb.

O tipo MIME de resposta HTTP é determinado por `fmt=` ou, se `fmt=` não for especificado, é `<image/jpeg>`.

O status da resposta HTTP será &#39;200 OK&#39; se o método de solicitação for um `GET` ou `HEAD` incondicional.

O servidor pode responder com o status &#39;304&#39; (não modificado) e não retornar nenhum dado de imagem em resposta a uma solicitação condicional `GET` (que inclui um cabeçalho válido `If-Modified-Since` ou `If-None-Match`).
