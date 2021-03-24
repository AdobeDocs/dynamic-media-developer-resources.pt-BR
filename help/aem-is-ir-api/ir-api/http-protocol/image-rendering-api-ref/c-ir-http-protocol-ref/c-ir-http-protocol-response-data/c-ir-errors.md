---
description: Se uma solicitação não puder ser concluída com êxito, o servidor retornará uma imagem de erro ou um status de resposta HTTP diferente de 200, junto com uma mensagem de erro.
solution: Experience Manager
title: Erros
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# Erros{#errors}

Se uma solicitação não puder ser concluída com êxito, o servidor retornará uma imagem de erro ou um status de resposta HTTP diferente de 200, junto com uma mensagem de erro.

O valor do status da resposta depende do tipo do erro; para a maioria dos erros comuns é &#39;403&#39;. As respostas de erro para tipos de solicitação que não são de imagem estão em conformidade com o formato especificado com `req=`. (Pode não ser implementado de forma consistente no momento.)

A quantidade de detalhes incluída na mensagem de erro é configurável com `attribute::ErrorDetail`.

**Imagens de erro**

O Image Serving pode ser configurado para retornar mensagens de erro renderizadas em uma imagem. Consulte `attribute::ErrorImage` na referência do catálogo de imagens para obter detalhes. Se a imagem de erro for gerada com êxito, o status da resposta HTTP será 200. Se ocorrer um erro ao processar a imagem de erro, a resposta de erro HTTP padrão e a mensagem de texto serão retornadas ao cliente.

**Consulte também**

[atributo::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ,  [atributo::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
