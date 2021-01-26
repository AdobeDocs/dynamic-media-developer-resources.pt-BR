---
description: Dados do conjunto de imagens. Fornece um mecanismo para definir conjuntos classificados de imagens e controlar atributos usados pelos visualizadores do Dynamic Media.
solution: Experience Manager
title: ImageSet
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---


# ImageSet{#imageset}

Dados do conjunto de imagens. Fornece um mecanismo para definir conjuntos classificados de imagens e controlar atributos usados pelos visualizadores do Dynamic Media.

Um conjunto de imagens consiste em uma lista de itens classificada, separada por vírgulas, com cada item consistindo em um ou mais sub-itens (IDs de imagem, IDs de amostra, caminhos de arquivos de mídia, rótulos etc.), separados por ponto-e-vírgula e/ou dois-pontos.

As chaves `{ }` e os parênteses `( )` podem ser usados para delimitar certos conteúdos (como valores de cor) ou indicar conjuntos aninhados. Os chaves ou parênteses usados dessa forma não devem ser codificados e devem sempre aparecer como pares correspondentes; caso contrário, ocorrerá um erro de análise de catálogo.

>[!NOTE]
>
>Os seguintes caracteres são usados como delimitadores definidos e devem ser codificados por HTTP quando aparecem no conjunto como parte dos valores de id ou string:
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



Consulte a documentação Visualizadores do Servidor de imagens para obter mais detalhes sobre a estrutura e o uso dos conjuntos de imagens.

O servidor retorna o conteúdo deste campo sem modificação em resposta a uma solicitação `req=imageset`.

## Conjuntos padrão {#section-5ecc8ffee7224668b63f601383665564}

As definições do conjunto a seguir são suportadas nativamente pelo Serviço de imagem, e o acesso a determinados visualizadores envolve análise, validação e processamento do conjunto pelo lado do servidor. Cada tipo de conjunto pode ser identificado especificando-se o valor correspondente em `catalog::AssetType`.

**Conjuntos básicos de amostras**

Cada item em um conjunto básico de amostras consiste em uma referência a um registro de imagem e uma referência separada opcional a um registro de imagem usado como uma amostra.

| `*`basicSwatchSet`*` | `*``*&#42;[',' *`swatchItemsWatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*``*[';' *`imageIdswatch`*]` |
| `*`amostra`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | Referência de imagem IS (catálogo/id) |
| `*`swatchId`*` | Referência de imagem IS (catálogo/id) |
| `*`solidColorSpecifier`*` | ` '{0x' *``* [ *`rotgbblabel`*]'}'` |
| `*`rrggbb`*` | Valor de cor hexadecimal RGB de 6 dígitos embalado para amostras de cores sólidas |
| `*`label`*` | Rótulo de texto opcional para amostras de cores sólidas |

**Conjuntos de amostras hierárquicas**

Cada item em um conjunto de amostras hierárquico pode consistir em um item de amostra básico ou uma referência a um registro de conjunto de amostras (são necessárias amostras para esses itens).

| `*`hierarchySwatchSet`*` | `*``* &#42;[ ',' *`hierárquicalSwatchItemHierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchySwatchItem`*` | `*``* | { *``* ';' *`swatchItembasicSwatchSetIdswatch`* }` |
| `*`basicSwatchSetId`*` | Referência IS (catálogo/id) para um registro de catálogo que define um conjunto básico de amostras |

**Conjuntos de rotação básicos**

Um conjunto de rotação básico consiste em uma lista simples de IDs de imagem.

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**Conjuntos de rotação bidimensionais**

Cada item em um conjunto de rotação bidimensional pode consistir em uma imagem simples, uma referência a um conjunto básico de rotação ou um conjunto básico de rotação em linha delimitado por chaves. Os parênteses podem ser usados em vez de chaves.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*``* | { '{' *``* '}' } | *`imageIdbasicSpinSetBasicSpinSetId`*` |
| `*`basicSpinSetId`*` | Referência IS (catálogo/id) para um registro de catálogo que define um conjunto de rotação básico |

**Conjuntos de páginas**

Cada item em um conjunto de páginas pode consistir em até três imagens de página separadas por dois pontos.

| `*`pageSet`*` | `*``* &#42;[ , *`pageItemItem`* ]` |
|---|---|
| `*`pageItem`*` | `*``* [ : *``* [ : *`imageIdimageIdimageId`* ] ]` |

**Conjuntos de mídia**

Cada item em um conjunto de mídia pode consistir em uma imagem, conjunto de amostras básico, conjunto de amostras hierárquico, conjunto de rotação básico, conjunto de rotação bidimensional, conjunto de páginas ou ativo de vídeo. Cada item de conjunto de mídia também pode conter uma amostra opcional e um identificador de tipo.

| `*`mediaSet`*` | `*`item `* &#42;[ , *`item`* ]` |
|---|---|
| `*`item`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemItemImageItemItemItemIDreserved`* ] ] ]` |
| `*`videoItem`*` | `*``* ; *`videoswatchId`*` |
| `*`recortItem`*` | `*``* ; *`rectswatchId`*` |
| `*`imageItem`*` | `*``* ; [ *`imageIdswatchId`* ]` |
| `*`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetWatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | ID da imagem IS |
| `*`video`*` | Caminho do arquivo de vídeo/animação ou ID do catálogo estático |
| `*`recuo`*` | Caminho do arquivo XML de definição de recebimento ou ID do catálogo estático |
| `*`imageId`*` | ID da imagem IS |
| `*`setId`*` | É referência a imagem, rotação ou conjunto de catálogo eletrônico |
| `*`inlineSet`*` | Imagem incorporada, rotação ou conjunto de catálogo eletrônico |
| `*`reserved`*` | Reservado para uso futuro |

**Conjuntos de vídeos**

Um conjunto de vídeos consiste em uma lista simples de ids de vídeo em que cada id faz referência a uma entrada no catálogo de conteúdo estático.

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## Propriedades {#section-17c731e5c46646aa90ac21f39bb693ca}

Sequência de caracteres de texto. Lista separada por vírgulas de valores `catalog::Id`, caminhos de arquivo absolutos do Servidor de imagens ou caminhos de arquivo relativos a `attribute::RootPath`. A mesma imagem pode ser referenciada mais de uma vez no conjunto. O registro de catálogo de definição pode aparecer no conjunto em qualquer local.

Esse campo participa da localização da string de texto. Além das strings *`label`* (parte de *`solidColorSpecifier`*), todos os campos delimitados são localizados se incluírem pelo menos um token de localização &#39; `^loc=…^`&#39;. Consulte [Localização de cadeia de caracteres de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) na *Referência de protocolo HTTP* para obter detalhes.

## Padrão {#section-c3a60e360393478284f0f2d2da5b963b}

Nenhum.

## Consulte Também {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [atributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), Tradução [ de Id de ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) objeto, Localização [ de string de ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) texto, Documentação de visualizadores do Servidor de imagens
