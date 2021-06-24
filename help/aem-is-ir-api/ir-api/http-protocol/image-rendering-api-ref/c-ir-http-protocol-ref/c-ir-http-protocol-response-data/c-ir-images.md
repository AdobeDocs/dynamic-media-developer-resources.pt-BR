---
description: Os dados da imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req= tiver um dos valores a seguir img, debug.
solution: Experience Manager
title: Imagens
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# Imagens{#images}

Os dados da imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req= tiver um dos seguintes valores: img, debug

O tipo MIME de resposta HTTP é determinado por `fmt=` ou, se `fmt=` não for especificado, depende do valor de `attribute::Format`.

O status da resposta HTTP será &#39;200 OK&#39; se o método de solicitação for um `GET` ou `HEAD` incondicional.

O servidor pode responder com o status &#39;304&#39; (não modificado) e não retornar nenhum dado de imagem em resposta a uma solicitação condicional `GET` (com o campo [!DNL If-Modified-Since] presente no `request-header`).
