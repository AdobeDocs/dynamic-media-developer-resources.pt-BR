---
description: Se uma solicitação não puder ser concluída com êxito, o servidor retornará uma imagem de erro ou um status de resposta HTTP diferente de 200, junto com uma mensagem de erro.
seo-description: Se uma solicitação não puder ser concluída com êxito, o servidor retornará uma imagem de erro ou um status de resposta HTTP diferente de 200, junto com uma mensagem de erro.
seo-title: Erros
solution: Experience Manager
title: Erros
uuid: a08f3f5a-3013-4d35-9612-25190a4c99fa
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---


# Erros{#errors}

Se uma solicitação não puder ser concluída com êxito, o servidor retornará uma imagem de erro ou um status de resposta HTTP diferente de 200, junto com uma mensagem de erro.

O valor do status da resposta depende do tipo do erro; para a maioria dos erros comuns é &#39;403&#39;. As respostas de erro para tipos de solicitação que não são de imagem estão em conformidade com o formato especificado com `req=`. (Pode não ser implementado de forma consistente no momento.)

A quantidade de detalhes incluída na mensagem de erro é configurável com `attribute::ErrorDetail`.

## Imagens de erro {#section-92e9b20b2507433daa96923abc95f777}

O Image Serving pode ser configurado para retornar mensagens de erro renderizadas em uma imagem.

Consulte [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) na referência do catálogo de imagens para obter detalhes.

Se a imagem de erro for gerada com êxito, o status da resposta HTTP será 200. Se ocorrer um erro ao processar a imagem de erro, a resposta de erro HTTP padrão e a mensagem de texto serão retornadas ao cliente.

## Imagem padrão {#section-66bf25fe6b434081bfae96d38d9be25e}

O Image Serving pode ser configurado para substituir uma imagem ausente por uma imagem padrão. A imagem padrão pode ser especificada com `attribute::DefaultImage` ou com o comando `defaultImage=`.

## Consulte também {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) ,  [atributo::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c),  [atributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
