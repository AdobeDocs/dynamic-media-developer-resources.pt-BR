---
title: ErrorImage
description: Imagem de resposta de erro. A Renderização de imagem normalmente retorna um status de erro com uma mensagem de texto quando ocorre um erro.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# ErrorImage {#errorimage}

Imagem de resposta de erro. A Renderização de imagem normalmente retorna um status de erro com uma mensagem de texto quando ocorre um erro. A variável `attribute::ErrorImage` permite que a configuração de uma imagem seja retornada se houver um erro.

Quando ocorre um erro, o servidor tenta interpretar o valor de `ImageRendering::attribute::ErrorImage`como um caminho de arquivo de imagem simples. Se não for possível abrir o arquivo, ele enviará o valor do atributo e os detalhes do erro para o Servidor de imagens, que processa conforme descrito em `ImageServing::attribute::ErrorImage`. Se o Servidor de imagens não retornar uma imagem de resposta válida, o status de erro HTTP padrão e a mensagem de texto serão enviados ao cliente.

Imagens de erro são retornadas com o status HTTP 200.

## Propriedades {#section-4a4a7e37ed11483db0b9922dc68ea7db}

String de texto. Se especificado, deve ser um **`ImageServing::catalog::id`** valor, um caminho relativo (para **`ImageServing::attribute::RootPath`** ou **`ImageRendering::attribute::RootPath`**), ou um caminho absoluto para um arquivo de imagem acessível pelo Servidor de imagens.

## Padrão {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Herdado de `default::ErrorImage` se não estiver definido. Se estiver definido, mas vazio, o comportamento da imagem de erro será desativado, mesmo se `default::ErrorImage` é definido e um status de erro HTTP é retornado.

## Consulte também {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [catálogo::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
