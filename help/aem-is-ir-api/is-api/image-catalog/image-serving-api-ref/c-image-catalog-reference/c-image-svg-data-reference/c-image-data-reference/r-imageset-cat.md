---
description: Dados do conjunto de imagens. Fornece um mecanismo para definir conjuntos classificados de imagens e controlar atributos usados pelos visualizadores do Dynamic Media.
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 0%

---

# ImageSet{#imageset}

Dados do conjunto de imagens. Fornece um mecanismo para definir conjuntos classificados de imagens e controlar atributos usados pelos visualizadores do Dynamic Media.

Um conjunto de imagens consiste em uma lista de itens classificados e separados por vírgulas. Cada item consiste em um ou mais subitens (IDs de imagem, IDs de amostra, caminhos de arquivo de mídia, rótulos e assim por diante), separados por ponto e vírgula, dois pontos ou ambos.

Chaves `{ }` e parênteses `( )` podem ser usados para delimitar determinado conteúdo (como valores de cor) ou indicar conjuntos aninhados. Chaves ou parênteses usados dessa maneira não devem ser codificados e devem sempre aparecer como pares correspondentes; caso contrário, ocorrerá um erro de análise de catálogo.

>[!NOTE]
>
>Os seguintes caracteres são usados como delimitadores de conjunto e devem ser codificados em HTTP quando aparecem no conjunto como parte de valores de id ou string:
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`


Consulte a documentação dos Visualizadores do servidor de imagens para obter detalhes adicionais sobre a estrutura e o uso de conjuntos de imagens.

O servidor retorna o conteúdo desse campo sem modificação em resposta a um `req=imageset` solicitação.

## Conjuntos Padrão {#section-5ecc8ffee7224668b63f601383665564}

As definições de conjunto a seguir são nativamente compatíveis com o Servidor de imagens, e o acesso com determinados visualizadores envolve a análise, validação e processamento do lado do servidor. Cada tipo de conjunto pode ser identificado especificando o valor correspondente em `catalog::AssetType`.

**Conjuntos de amostras básicos**

Cada item em um conjunto de amostras básico consiste em uma referência a um registro de imagem e uma referência separada opcional a um registro de imagem usado como amostra.

| `*`basicSwatchSet`*` | `*`swatchItem`*&#42;[',' *`swatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*`imageId`*[';' *`amostra`*]` |
| `*`amostra`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | Referência da imagem IS (catálogo/id) |
| `*`swatchId`*` | Referência da imagem IS (catálogo/id) |
| `*`solidColorSpecifier`*` | ` '{0x' *`rrggbb`* [ *`rótulo`*]'}'` |
| `*`rrggbb`*` | Valor de cor de RGB hexadecimal de 6 dígitos compactado para amostras de cores sólidas |
| `*`rótulo`*` | Rótulo de texto opcional para amostras de cores sólidas |

**Conjuntos de amostras hierárquicas**

Cada item em um conjunto de amostras hierárquico pode consistir em um item de amostra básico ou uma referência a um registro de conjunto de amostras (as amostras são necessárias para esses itens).

| `*`hierarchicalSwatchSet`*` | `*`hierarchicalSwatchItem`* &#42;[ ',' *`hierarchicalSwatchItem`* ]` |
|---|---|
| `*`hierarchicalSwatchItem`*` | `*`swatchItem`* | { *`basicSwatchSetId`* ';' *`amostra`* }` |
| `*`basicSwatchSetId`*` | Referência IS (catálogo/id) a um registro de catálogo que define um conjunto de amostras básico |

**Conjuntos de rotação básicos**

Um conjunto de rotação básico consiste em uma lista simples de IDs de imagem.

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**Conjuntos de rotação bidimensionais**

Cada item em um conjunto de rotação bidimensional pode consistir em uma imagem simples, uma referência a um conjunto de rotação básico ou um conjunto de rotação básico em linha delimitado por chaves. É possível usar parênteses em vez de chaves.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`* | { '{' *`basicSpinSet`* '}' } | *`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | Referência IS (catálogo/id) a um registro de catálogo que define um conjunto de rotação básico |

**Conjuntos de páginas**

Cada item em um conjunto de páginas pode consistir em imagens de até três páginas separadas por dois pontos.

| `*`pageSet`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**Conjuntos de mídia**

Cada item em um conjunto de mídia pode consistir em uma imagem, um conjunto de amostras básico, um conjunto de amostras hierárquico, um conjunto de rotação básico, um conjunto de rotação bidimensional, um conjunto de páginas ou um ativo de vídeo. Cada item do conjunto de mídia também pode conter um identificador opcional de amostra e tipo.

| `*`mediaSet`*` | `*`item`* &#42;[ , *`item`* ]` |
|---|---|
| `*`item`*` | ` { *`videoItem`* | *`recutItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`reservado`* ] ] ]` |
| `*`videoItem`*` | `*`vídeo`* ; *`swatchId`*` |
| `*`recutItem`*` | `*`recortar`* ; *`swatchId`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`swatchId`* ]` |
| `*`setItem`*` | ` { *`setId`* | { '{' *`inlineSet`* '}' } } ; *`swatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | Id da imagem IS |
| `*`vídeo`*` | Caminho do arquivo de vídeo/animação ou ID estática do catálogo |
| `*`recortar`*` | Caminho do arquivo XML de definição do registro ou ID estática do catálogo |
| `*`imageId`*` | Id da imagem IS |
| `*`setId`*` | Referência IS para imagem, rotação ou conjunto ecatalog |
| `*`inlineSet`*` | Imagem embutida, rotação ou conjunto de catálogo eletrônico |
| `*`reservado`*` | Reservado para uso futuro |

**Conjuntos de vídeos**

Um conjunto de vídeos consiste em uma lista simples de ids de vídeo em que cada id faz referência a uma entrada no catálogo de conteúdo estático.

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## Propriedades {#section-17c731e5c46646aa90ac21f39bb693ca}

String de texto. Lista separada por vírgulas de `catalog::Id` valores, caminhos de arquivo absolutos do Servidor de imagens ou caminhos de arquivo relativos a `attribute::RootPath`. A mesma imagem pode ser referenciada mais de uma vez no conjunto. O registro de catálogo de definição pode aparecer no conjunto em qualquer local.

Este campo participa da localização da sequência de caracteres de texto. Além de *`label`* strings (parte do *`solidColorSpecifier`*) todos os campos delimitados são localizados se incluírem pelo menos um &#39; `^loc=…^`token de localização &#39;. Consulte [Localização da sequência de caracteres de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) no *Referência de protocolo HTTP* para obter detalhes.

## Padrão {#section-c3a60e360393478284f0f2d2da5b963b}

Nenhum.

## Consulte Também {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), [Conversão Da Id Do Objeto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) , [Localização da sequência de caracteres de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Documentação De Visualizadores Do Servidor De Imagens
