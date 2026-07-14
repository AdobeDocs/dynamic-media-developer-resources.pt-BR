---
title: Imagens
description: Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req= tiver um dos valores img, debug abaixo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 089aaf9d-f414-4ca4-9d6d-7f429de2531e
TQID: 'https://experienceleague.adobe.com/4wHyyXX0gxz9ojr5g5Puu5fBhKXo4hZDjyBuVTao3rQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# Imagens{#images}

Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req= tiver um dos seguintes valores: img, debug

O tipo MIME da resposta HTTP é determinado por `fmt=`, ou, se `fmt=` não for especificado, depende do valor de `attribute::Format`.

O status da resposta HTTP é &#39;200 OK&#39; se o método de solicitação era um incondicional `GET` ou `HEAD`.

O servidor pode responder com o status &#39;304&#39; (não modificado) e não retornar dados de imagem em resposta a uma solicitação condicional `GET` (com o campo [!DNL If-Modified-Since] presente em `request-header`).

