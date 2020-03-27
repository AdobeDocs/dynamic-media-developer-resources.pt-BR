---
description: Imagem de resposta de erro. O Serviço de imagem normalmente retorna um status de erro com uma mensagem de texto quando ocorre um erro.
seo-description: Imagem de resposta de erro. O Serviço de imagem normalmente retorna um status de erro com uma mensagem de texto quando ocorre um erro.
seo-title: ErrorImage
solution: Experience Manager
title: ErrorImage
topic: Scene7 Image Serving - Image Rendering API
uuid: b071c0cd-e7b8-422b-9b23-d93f504d9ce5
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# ErrorImage{#errorimage}

Imagem de resposta de erro. O Serviço de imagem normalmente retorna um status de erro com uma mensagem de texto quando ocorre um erro.

`attribute::ErrorImage` permite que a configuração de uma imagem, entrada de catálogo ou modelo seja retornada em caso de erro.

>[!NOTE]
>
>Imagens ausentes também podem ser tratadas com `attribute::DefaultImage`.

É possível configurar um modelo do Servidor de imagens que pode renderizar o texto da mensagem de erro na imagem de resposta. As variáveis predefinidas a seguir podem ser incluídas no `$error.title` modelo, que é substituído por uma breve descrição de erro, e `$error.message`, que é substituída por uma descrição de erro mais detalhada (o nível de detalhes está configurado com `attribute::ErrorDetail`).

O status HTTP 200 será retornado se a imagem/modelo de erro puder ser processado com êxito. Se ocorrer um erro durante esse processamento, o status do erro HTTP e uma mensagem de texto serão retornados.

## Propriedades {#section-f460c6c2dd1f46b29f9a79b093575f45}

Sequência de caracteres de texto. Se especificado, deve ser um valor de catálogo válido::Id em um catálogo de imagens ou um caminho relativo (para `attribute::RootPath`) ou absoluto para um arquivo de imagem acessível pelo Servidor de imagens.

## Padrão {#section-2885f289e5714ddca665a6aee401967f}

Herdado de `default::ErrorImage` se não estiver definido. Se definido, mas vazio, o comportamento da imagem de erro é desativado, mesmo se `default::ErrorImage` estiver definido, e um status de erro HTTP e uma mensagem de texto são retornados.

## Example {#section-c92090abe1d247529542a8dd4960c2e6}

Para obter imagens de resposta com a mensagem de erro renderizada na imagem, primeiro precisamos definir o modelo no catálogo de imagens. Nesse caso, criamos uma entrada em nosso catálogo de imagens chamada `onError`, contendo o seguinte em `catalog::Modifier`:

`size=300,300&bgc=ffffff&text=$error.message$`

O modelo está registrado com `attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

Neste exemplo, o texto será renderizado usando a fonte padrão, a cor da fonte e o tamanho da fonte.

## Consulte também {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) , [catálogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [atributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [atributo::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
