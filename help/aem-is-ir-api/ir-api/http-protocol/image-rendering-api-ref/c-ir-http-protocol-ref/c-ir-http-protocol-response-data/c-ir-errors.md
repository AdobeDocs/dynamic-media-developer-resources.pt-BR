---
description: Se uma solicitação não puder ser concluída com êxito, o servidor retornará uma imagem de erro ou um status de resposta HTTP diferente de 200, juntamente com uma mensagem de erro.
seo-description: Se uma solicitação não puder ser concluída com êxito, o servidor retornará uma imagem de erro ou um status de resposta HTTP diferente de 200, juntamente com uma mensagem de erro.
seo-title: Erros
solution: Experience Manager
title: Erros
topic: Scene7 Image Serving - Image Rendering API
uuid: 5984fa9e-63c8-426b-be5f-48f66fc918c3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Erros{#errors}

Se uma solicitação não puder ser concluída com êxito, o servidor retornará uma imagem de erro ou um status de resposta HTTP diferente de 200, juntamente com uma mensagem de erro.

O valor do status da resposta depende do tipo de erro; para a maioria dos erros comuns é &quot;403&quot;. Respostas de erro para tipos de solicitação que não sejam de imagem estão em conformidade com o formato especificado com `req=`. (Pode não ser implementado consistentemente no momento.)

A quantidade de detalhes incluída na mensagem de erro é configurável com `attribute::ErrorDetail`.

**Imagens de erro**

O Serviço de imagem pode ser configurado para retornar mensagens de erro renderizadas em uma imagem. Consulte `attribute::ErrorImage` na referência do catálogo de imagens para obter detalhes. Se a imagem de erro for gerada com êxito, o status da resposta HTTP será 200. Se ocorrer um erro ao processar a imagem de erro, a resposta de erro HTTP padrão e a mensagem de texto serão retornadas ao cliente.

**Consulte também**

[atributo::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ,  [atributo::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
