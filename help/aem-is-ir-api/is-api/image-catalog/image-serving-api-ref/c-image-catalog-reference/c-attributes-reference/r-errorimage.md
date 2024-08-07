---
description: Imagem de resposta de erro. O Servidor de imagens normalmente retorna um status de erro com uma mensagem de texto quando ocorre um erro.
solution: Experience Manager
title: ErrorImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f412a379-525e-42fc-97bf-b10e00da6a20
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# ErrorImage{#errorimage}

Imagem de resposta de erro. O Servidor de imagens normalmente retorna um status de erro com uma mensagem de texto quando ocorre um erro.

`attribute::ErrorImage` permite que a configuração de uma imagem, entrada de catálogo ou modelo seja retornada em caso de erro.

>[!NOTE]
>
>Imagens ausentes também podem ser tratadas com `attribute::DefaultImage`.

Um modelo do Servidor de imagens pode ser configurado, o que pode renderizar o texto da mensagem de erro na imagem de resposta. As variáveis predefinidas a seguir podem ser incluídas no modelo `$error.title`, que é substituído por uma breve descrição do erro, e `$error.message`, que é substituído por uma descrição mais detalhada do erro (o nível de detalhes é configurado com `attribute::ErrorDetail`).

O status HTTP 200 será retornado se a imagem/modelo de erro puder ser processada com êxito. Se ocorrer um erro durante esse processamento, o status do erro HTTP e uma mensagem de texto serão retornados.

## Propriedades {#section-f460c6c2dd1f46b29f9a79b093575f45}

String de texto. Se especificado, deve ser um valor catalog::Id válido em um catálogo de imagens ou um caminho relativo (para `attribute::RootPath`) ou absoluto para um arquivo de imagem acessível pelo Servidor de Imagens.

## Padrão {#section-2885f289e5714ddca665a6aee401967f}

Herdado de `default::ErrorImage` se não estiver definido. Se definido, mas vazio, o comportamento da imagem de erro é desabilitado, mesmo se `default::ErrorImage` for definido, e um status de erro HTTP e uma mensagem de texto são retornados.

## Exemplo {#section-c92090abe1d247529542a8dd4960c2e6}

Para obter imagens de resposta com a mensagem de erro renderizada na imagem, primeiro devemos definir o modelo no catálogo de imagens. Nesse caso, criamos uma entrada em nosso catálogo de imagens chamada `onError`, contendo o seguinte em `catalog::Modifier`:

`size=300,300&bgc=ffffff&text=$error.message$`

O modelo está registrado com `attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

Para este exemplo, o texto é renderizado usando a fonte padrão, a cor da fonte e o tamanho da fonte.

## Consulte também {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) , [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
