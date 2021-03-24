---
description: Os dados da imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req= tiver um dos valores a seguir img, debug
solution: Experience Manager
title: Imagens
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---


# Imagens{#images}

Os dados da imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req= tiver um dos seguintes valores: img, debug

O tipo MIME de resposta HTTP é determinado por `fmt=` ou, se `fmt=` não for especificado, depende do valor de `attribute::Format`.

O status da resposta HTTP será &#39;200 OK&#39; se o método de solicitação for um `GET` ou `HEAD` incondicional.

O servidor pode responder com o status &#39;304&#39; (não modificado) e não retornar nenhum dado de imagem em resposta a uma solicitação condicional `GET` (com o campo [!DNL If-Modified-Since] presente no `request-header`).
