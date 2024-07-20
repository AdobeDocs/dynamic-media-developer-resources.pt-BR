---
title: Imagens
description: Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req= tiver um dos valores img, debug abaixo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Imagens{#images}

Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req= tiver um dos seguintes valores: img, debug

O tipo MIME da resposta HTTP é determinado por `fmt=`, ou, se `fmt=` não for especificado, depende do valor de `attribute::Format`.

O status da resposta HTTP é &#39;200 OK&#39; se o método de solicitação era um incondicional `GET` ou `HEAD`.

O servidor pode responder com o status &#39;304&#39; (não modificado) e não retornar dados de imagem em resposta a uma solicitação condicional `GET` (com o campo [!DNL If-Modified-Since] presente em `request-header`).
