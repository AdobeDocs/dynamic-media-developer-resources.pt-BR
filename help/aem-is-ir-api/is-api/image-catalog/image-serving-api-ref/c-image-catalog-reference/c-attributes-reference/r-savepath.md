---
description: Caminho raiz para saveToFile=. Caminho relativo da pasta raiz na qual as imagens geradas com req=saveToFile devem ser gravadas.
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 0%

---

# SavePath{#savepath}

Caminho raiz para saveToFile=. Caminho relativo da pasta raiz na qual as imagens geradas com req=saveToFile devem ser gravadas.

`SavePath` é um valor de string de texto.

## Propriedades {#section-343d1371e966491c92854a8df14c3c50}

Sequência de texto. Deve estar vazio ou ser um caminho de pasta relativo válido. Sempre combinado com o caminho raiz absoluto configurado com `ImageServer::SaveDirectory`.

## Padrão {#section-ae751eea97654f399c6aaee3f3252cbb}

Herdado de `default::SavePath` se não estiver definido. Salvar em arquivos estará desativado se o valor resultante estiver vazio.

## Consulte também {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
