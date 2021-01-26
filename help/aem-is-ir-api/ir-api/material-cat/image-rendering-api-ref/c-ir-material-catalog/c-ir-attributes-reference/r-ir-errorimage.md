---
description: Imagem de resposta de erro. A renderização de imagem normalmente retorna um status de erro com uma mensagem de texto quando ocorre um erro. attribute ErrorImage permite que a configuração de uma imagem seja retornada em caso de erro.
seo-description: Imagem de resposta de erro. A renderização de imagem normalmente retorna um status de erro com uma mensagem de texto quando ocorre um erro. attribute ErrorImage permite que a configuração de uma imagem seja retornada em caso de erro.
seo-title: ErrorImage *
solution: Experience Manager
title: ErrorImage *
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6c8801d0-8cd0-4477-9a60-ccbb343a0747
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---


# ErrorImage *{#errorimage}

Imagem de resposta de erro. A renderização de imagem normalmente retorna um status de erro com uma mensagem de texto quando ocorre um erro. attribute::ErrorImage permite que a configuração de uma imagem seja retornada em caso de erro.

Quando ocorre um erro, o servidor primeiro tenta interpretar o valor de `ImageRendering::attribute::ErrorImage`como um caminho de arquivo de imagem simples. Se o arquivo não puder ser aberto, ele enviará o valor do atributo e os detalhes do erro para o Serviço de imagem, que processa conforme descrito em `ImageServing::attribute::ErrorImage`. Se o Serviço de imagem não retornar uma imagem de resposta válida, o status de erro HTTP padrão e a mensagem de texto serão enviados ao cliente.

As imagens de erro são retornadas com o status HTTP 200.

## Propriedades {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Sequência de caracteres de texto. Se especificado, deve ser um valor **`ImageServing::catalog::id`**, um caminho relativo (para **`ImageServing::attribute::RootPath`** ou **`ImageRendering::attribute::RootPath`**) ou um caminho absoluto para um arquivo de imagem que seja acessível pelo Servidor de imagens.

## Padrão {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Herdado de `default::ErrorImage` se não estiver definido. Se estiver definido, mas vazio, o comportamento da imagem de erro será desativado, mesmo se `default::ErrorImage` estiver definido e um status de erro HTTP será retornado.

## Consulte também {#section-3e0308eaf4124451909dacd570e27695}

[atributo::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [atributo::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catálogo::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
