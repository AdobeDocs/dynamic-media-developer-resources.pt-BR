---
description: Caminho raiz para saveToFile=. Caminho relativo da pasta raiz na qual as imagens geradas com req=saveToFile devem ser gravadas.
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
TQID: 'https://experienceleague.adobe.com/CXC5-22MiZRyIjwOgOcgpRGq6kVZSZ6S-EKq8N-k7ME'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 0%

---

# SavePath{#savepath}

Caminho raiz para saveToFile=. Caminho relativo da pasta raiz na qual as imagens geradas com req=saveToFile devem ser gravadas.

`SavePath` é um valor de cadeia de texto.

## Propriedades {#section-343d1371e966491c92854a8df14c3c50}

String de texto. Deve ser um caminho de pasta relativo ou vazio. Sempre combinado com o caminho raiz absoluto configurado com `ImageServer::SaveDirectory`.

## Padrão {#section-ae751eea97654f399c6aaee3f3252cbb}

Herdado de `default::SavePath` se não estiver definido. Salvar em arquivos será desativado se o valor resolvido estiver vazio.

## Consulte também {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
