---
description: Imagem de resposta do erro. A renderização de imagem normalmente retorna um status de erro com uma mensagem de texto quando ocorre um erro. O atributo ErrorImage permite que a configuração de uma imagem seja retornada em caso de erro.
solution: Experience Manager
title: ErrorImage *
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# ErrorImage *{#errorimage}

Imagem de resposta do erro. A renderização de imagem normalmente retorna um status de erro com uma mensagem de texto quando ocorre um erro. attribute::ErrorImage permite que a configuração de uma imagem seja retornada em caso de erro.

Quando ocorre um erro, o servidor tenta primeiro interpretar o valor de `ImageRendering::attribute::ErrorImage`como um caminho de arquivo de imagem simples. Se o arquivo não puder ser aberto, ele enviará o valor do atributo e os detalhes do erro para o Serviço de imagem, que processa conforme descrito em `ImageServing::attribute::ErrorImage`. Se a Exibição de imagem não retornar uma imagem de resposta válida, o status de erro HTTP padrão e a mensagem de texto serão enviados ao cliente.

Imagens de erro são retornadas com o status HTTP 200.

## Propriedades {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Sequência de texto. Se especificado, deve ser um valor **`ImageServing::catalog::id`**, um caminho relativo (para **`ImageServing::attribute::RootPath`** ou **`ImageRendering::attribute::RootPath`**) ou um caminho absoluto para um arquivo de imagem que seja acessível pelo Servidor de Imagens.

## Padrão {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Herdado de `default::ErrorImage` se não estiver definido. Se estiver definido, mas estiver vazio, o comportamento da imagem de erro será desativado, mesmo que `default::ErrorImage` esteja definido, e um status de erro HTTP será retornado.

## Consulte também {#section-3e0308eaf4124451909dacd570e27695}

[atributo::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [atributo::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catálogo::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
