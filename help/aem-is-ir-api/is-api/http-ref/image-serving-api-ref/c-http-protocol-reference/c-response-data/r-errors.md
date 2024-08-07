---
description: Se uma solicitação não puder ser concluída com êxito, o servidor retornará uma imagem de erro ou um status de resposta HTTP diferente de 200, juntamente com uma mensagem de erro.
solution: Experience Manager
title: Erros
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Erros{#errors}

Se uma solicitação não puder ser concluída com êxito, o servidor retornará uma imagem de erro ou um status de resposta HTTP diferente de 200, juntamente com uma mensagem de erro.

O valor do status de resposta depende do tipo do erro; para os erros mais comuns, é &#39;403&#39;. As respostas de erro para tipos de solicitação que não são de imagem estão em conformidade com o formato especificado com `req=`. (Pode não ser implementado de forma consistente neste momento.)

A quantidade de detalhes incluída na mensagem de erro é configurável com `attribute::ErrorDetail`.

## Imagens de erro {#section-92e9b20b2507433daa96923abc95f777}

O Servidor de imagens pode ser configurado para retornar mensagens de erro renderizadas em uma imagem.

Consulte [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) na referência de catálogo de imagens para obter detalhes.

Se a imagem de erro for gerada com êxito, o status da resposta HTTP será 200. Se ocorrer um erro ao processar a imagem de erro, a resposta de erro HTTP padrão e a mensagem de texto serão retornadas ao cliente.

## Imagem padrão {#section-66bf25fe6b434081bfae96d38d9be25e}

O Servidor de imagens pode ser configurado para substituir uma imagem ausente por uma imagem padrão. A imagem padrão pode ser especificada com o comando `attribute::DefaultImage` ou `defaultImage=`.

## Consulte também {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) , [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
