---
description: Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req=img ou req=tmb.
solution: Experience Manager
title: Imagens
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---

# Imagens{#images}

Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req=img ou req=tmb.

O tipo de MIME da resposta HTTP é determinado por `fmt=`, ou, se `fmt=` não for especificado, será `<image/jpeg>`.

O status da resposta HTTP é &#39;200 OK&#39; se o método de solicitação era incondicional `GET` ou `HEAD`.

O servidor pode responder com o status &#39;304&#39; (não modificado) e não retornar dados de imagem em resposta a uma condição `GET` (que inclui uma licença `If-Modified-Since` ou `If-None-Match` cabeçalho).
