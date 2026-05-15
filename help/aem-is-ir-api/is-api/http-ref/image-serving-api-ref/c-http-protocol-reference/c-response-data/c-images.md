---
description: Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req=img ou req=tmb.
solution: Experience Manager
title: Imagens
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3aa46d48-82eb-4a21-a5e5-b33904b97888
TQID: 'https://experienceleague.adobe.com/1tStTbuCLrOG8XrPgOw5qH-VujpHXX8Pt0IWXg9329Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 0%

---

# Imagens{#images}

Os dados de imagem são retornados se uma solicitação for concluída com êxito e se a solicitação não incluir um comando req= ou se req=img ou req=tmb.

O tipo MIME da resposta HTTP é determinado por `fmt=` ou, se `fmt=` não for especificado, é `<image/jpeg>`.

O status da resposta HTTP é &#39;200 OK&#39; se o método de solicitação era um incondicional `GET` ou `HEAD`.

O servidor pode responder com o status &#39;304&#39; (não modificado) e não retornar dados de imagem em resposta a uma solicitação condicional `GET` (que inclui um cabeçalho `If-Modified-Since` ou `If-None-Match` válido).
