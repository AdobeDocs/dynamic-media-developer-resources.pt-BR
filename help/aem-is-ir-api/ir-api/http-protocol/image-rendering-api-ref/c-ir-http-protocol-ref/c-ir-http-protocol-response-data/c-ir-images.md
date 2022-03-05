---
title: Imagens
description: Os dados da imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req= tiver um dos valores a seguir img, debug.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Imagens{#images}

Os dados da imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req= tiver um dos seguintes valores: img, debug

O tipo MIME da resposta HTTP é determinado por `fmt=`ou, se `fmt=` não for especificado, depende do valor de `attribute::Format`.

O status da resposta HTTP será &#39;200 OK&#39; se o método de solicitação for incondicional `GET` ou `HEAD`.

O servidor pode responder com o status &#39;304&#39; (não modificado) e não retornar nenhum dado de imagem em resposta a um condicional `GET` (com [!DNL If-Modified-Since] no campo `request-header`).
