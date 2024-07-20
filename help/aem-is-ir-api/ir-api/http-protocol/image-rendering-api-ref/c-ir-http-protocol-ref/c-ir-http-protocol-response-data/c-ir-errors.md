---
title: Erros
description: Se uma solicitação não puder ser concluída com êxito, o servidor retornará uma imagem de erro ou um status de resposta HTTP diferente de 200, juntamente com uma mensagem de erro.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# Erros{#errors}

Se uma solicitação não puder ser concluída com êxito, o servidor retornará uma imagem de erro ou um status de resposta HTTP diferente de 200, juntamente com uma mensagem de erro.

O valor do status de resposta depende do tipo do erro; para os erros mais comuns, é &#39;403&#39;. As respostas de erro para tipos de solicitação que não são de imagem estão em conformidade com o formato especificado com `req=`. (Pode não ser implementado de forma consistente no momento.)

A quantidade de detalhes incluída na mensagem de erro é configurável com `attribute::ErrorDetail`.

**Imagens de erro**

O Servidor de imagens pode ser configurado para retornar mensagens de erro renderizadas em uma imagem. Consulte `attribute::ErrorImage` na referência do catálogo de imagens para obter detalhes. Se a imagem de erro for gerada com êxito, o status da resposta HTTP será 200. Se ocorrer um erro ao processar a imagem de erro, a resposta de erro HTTP padrão e a mensagem de texto serão retornadas ao cliente.

**Consulte também**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
