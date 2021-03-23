---
description: Dados do conjunto de imagens. Fornece um mecanismo para definir conjuntos classificados de imagens e atributos de controle usados pelos visualizadores do Dynamic Media.
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic, SDK/API, Conjuntos de imagens
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---


# ImageSet{#imageset}

Dados do conjunto de imagens. Fornece um mecanismo para definir conjuntos classificados de imagens e atributos de controle usados pelos visualizadores do Dynamic Media.

Um conjunto de imagens consiste em uma lista de itens classificada, separada por vírgulas, com cada item consistindo em um ou mais sub-itens (ids de imagem, ids de amostra, caminhos de arquivo de mídia, rótulos etc.), separados por ponto-e-vírgula e/ou dois pontos.

As chaves `{ }` e os parênteses `( )` podem ser usados para delimitar determinados conteúdos (como valores de cor) ou indicar conjuntos aninhados. As chaves ou os parênteses usados dessa forma não devem ser codificados e devem sempre aparecer como pares correspondentes; caso contrário, ocorrerá um erro de análise de catálogo.

>[!NOTE]
>
>Os caracteres a seguir são usados como delimitadores de conjunto e devem ser codificados por HTTP quando aparecem no conjunto como parte dos valores id ou string:
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



Consulte a documentação dos visualizadores do fornecimento de imagens para obter detalhes adicionais sobre a estrutura e o uso dos conjuntos de imagens.

O servidor retorna o conteúdo desse campo sem modificação em resposta a uma solicitação `req=imageset`.

## Conjuntos Padrão {#section-5ecc8ffee7224668b63f601383665564}

As definições do conjunto a seguir são nativamente compatíveis com o Serviço de imagem e o acesso a determinados visualizadores envolve análise, validação e processamento do conjunto pelo lado do servidor. Cada tipo de conjunto pode ser identificado especificando o valor correspondente em `catalog::AssetType`.

**Conjuntos de amostras básicas**

Cada item em um conjunto básico de amostras consiste em uma referência a um registro de imagem e uma referência separada opcional a um registro de imagem usado como amostra.

| `*`basicSwatchSet`*` | `*``*&#42;[',' *`swatchItemswatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*``*[';' *`imageIdswatch`*]` |
| `*`amostra`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | Referência de imagem IS (catálogo/id) |
| `*`swatchId`*` | Referência de imagem IS (catálogo/id) |
| `*`solidColorSpecifier`*` | ` '{0x' *``* [ *`rgbblabel`*]'}'` |
| `*`rrggbb`*` | Valor de cor RGB hexadecimal de 6 dígitos embalado para amostras de cores sólidas |
| `*`label`*` | Rótulo de texto opcional para amostras de cores sólidas |

**Conjuntos de amostras hierárquicas**

Cada item em um conjunto de amostras hierárquico pode consistir em um item de amostra básico ou uma referência a um registro de conjunto de amostras (são necessárias amostras para esses itens).

| `*`hiericalSwatchSet`*` | `*``* &#42;[ ',' *`hierárquicalSwatchItemhierárquicalSwatchItem`* ]` |
|---|---|
| `*`primarySwatchItem`*` | `*``* | { *``* ';' *`swatchEmbasicSwatchSetIdswatch`* }` |
| `*`basicSwatchSetId`*` | Referência IS (catálogo/id) a um registro de catálogo que define um conjunto de amostras básico |

**Conjuntos básicos de rotação**

Um conjunto de rotação básico consiste em uma lista simples de IDs de imagem.

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**Conjuntos de rotação bidimensionais**

Cada item em um conjunto de rotação bidimensional pode consistir em uma imagem simples, uma referência a um conjunto de rotação básico ou um conjunto de rotação básico em linha delimitado por chaves. Os parênteses podem ser usados em vez de chaves.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| `*`basicSpinSetId`*` | Referência IS (catálogo/id) a um registro de catálogo que define um conjunto de rotação básico |

**Conjuntos de páginas**

Cada item em um conjunto de páginas pode consistir em até três imagens de página separadas por dois pontos.

| `*`pageSet`*` | `*``* &#42;[ , *`pageItempageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*``* [ : *``* [ : *`imageIdimageIdimageId`* ] ]` |

**Conjuntos de mídia**

Cada item em um conjunto de mídia pode consistir em uma imagem, conjunto de amostras básico, conjunto de amostras hierárquico, conjunto de rotação básico, conjunto de rotação bidimensional, conjunto de páginas ou ativo de vídeo. Cada item do conjunto de mídia também pode conter uma amostra e um identificador de tipo opcionais.

| `*`mediaSet`*` | `*``* &#42;[ , *`item`* ]` |
|---|---|
| `*`item`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemrecutItemimageItemsetItemIDreserved`* ] ] ]` |
| `*`videoItem`*` | `*``* ; *`videoswatchId`*` |
| `*`rectItem`*` | `*``* ; *`recutswatchId`*` |
| `*`imageItem`*` | `*``* ; [ *`imageIdswatchId`* ]` |
| `*`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | ID da imagem IS |
| `*`vídeo`*` | Caminho do arquivo de vídeo/animação ou ID do catálogo estático |
| `*`recuo`*` | Caminho do arquivo XML de definição de receita ou ID do catálogo estático |
| `*`imageId`*` | ID da imagem IS |
| `*`setId`*` | IS referência a imagem, rotação ou conjunto de catálogo eletrônico |
| `*`inlineSet`*` | Imagem embutida, rotação ou conjunto de catálogo eletrônico |
| `*`reservado`*` | Reservado para uso futuro |

**Conjuntos de vídeos**

Um conjunto de vídeos consiste em uma lista simples de ids de vídeo em que cada id faz referência a uma entrada no catálogo de conteúdo estático.

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## Propriedades {#section-17c731e5c46646aa90ac21f39bb693ca}

Sequência de texto. Lista separada por vírgulas de valores `catalog::Id`, caminhos de arquivo absolutos do Servidor de imagem ou caminhos de arquivo relativos a `attribute::RootPath`. A mesma imagem pode ser referenciada mais de uma vez no conjunto. O registro de catálogo de definição pode aparecer no conjunto em qualquer local.

Esse campo participa da localização da string de texto. Além das strings *`label`* (parte do *`solidColorSpecifier`*), todos os campos delimitados são localizados se incluírem pelo menos um token de localização &#39; `^loc=…^`&#39;. Consulte [Localização da cadeia de caracteres de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) no *Referência do protocolo HTTP* para obter detalhes.

## Padrão {#section-c3a60e360393478284f0f2d2da5b963b}

Nenhum.

## Consulte também {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [atributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), Tradução da ID do  [objeto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) , Localização da sequência de  [texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Documentação dos visualizadores do servidor de imagens
