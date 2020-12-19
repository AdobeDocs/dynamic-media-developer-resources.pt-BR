---
description: O Serviço de imagem fornece um mecanismo para buscar uma resposta de texto hierárquica (xml ou json) que representa todos os recursos e metadados associados ao ImageSet do catálogo para um registro específico.
seo-description: O Serviço de imagem fornece um mecanismo para buscar uma resposta de texto hierárquica (xml ou json) que representa todos os recursos e metadados associados ao ImageSet do catálogo para um registro específico.
seo-title: Solicitações de conjunto de mídia
solution: Experience Manager
title: Solicitações de conjunto de mídia
topic: Scene7 Image Serving - Image Rendering API
uuid: af9fabcd-531d-43fb-bd97-269923bea5e8
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Solicitações de conjunto de mídia{#media-set-requests}

O Serviço de imagem fornece um mecanismo para buscar uma resposta de texto hierárquica (xml ou json) que representa todos os recursos e metadados associados ao catálogo::ImageSet para um registro específico.

Os visualizadores podem usar esse mecanismo para gerar respostas para informar a apresentação de imagens simples, vídeos, conjuntos de vídeo, conjuntos de amostras, conjuntos de rotação, conjuntos de páginas (e-catalogs) e conjuntos de mídia.

## Sintaxe de solicitação {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

A resposta definida para um `catalog::ImageSet` pode ser recuperada usando o modificador `req=set` e referenciando a id de registro do catálogo no caminho de rede. Como alternativa, o conjunto de imagens pode ser especificado diretamente no URL usando o modificador `imageset=`. Se o modificador `imageset=` for usado para especificar o conjunto de imagens, todo o valor deverá estar entre chaves para escapar do valor do conjunto de imagens e garantir que todos os modificadores incluídos não sejam interpretados como parte da string do query URL.

## Tipos de respostas definidas {#section-93eb0a1f70344da2a888e56372ad3896}

O mecanismo set suporta os seguintes tipos de respostas:

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>imagens simples </p></td> 
  <td class="stentry"> <p>Um registro de imagem sem <span class="codeph"> catálogo::ImageSet</span> definido. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>vídeos simples </p></td> 
  <td class="stentry"> <p>Um registro de vídeo no catálogo de conteúdo estático. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de amostras </p></td> 
  <td class="stentry"> <p>Um conjunto de itens que consiste em uma referência a um registro de imagem e uma referência separada opcional a um registro de imagem usado como amostra. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de amostras hierárquicas </p></td> 
  <td class="stentry"> <p>Um conjunto de itens que consiste em um item de amostra básico ou uma referência a um registro de conjunto de amostras. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de rotação </p></td> 
  <td class="stentry"> <p>Um conjunto de itens que consiste em uma lista simples de IDs de imagem. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de rotação bidimensionais </p></td> 
  <td class="stentry"> <p>Um conjunto de itens que consiste em uma imagem simples ou uma referência a um conjunto de rotação básico. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de páginas </p></td> 
  <td class="stentry"> <p>Um conjunto de itens que consiste em uma lista de até três imagens de página </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de mídia </p></td> 
  <td class="stentry"> <p>Um conjunto de itens que consiste em imagens simples, conjuntos de vídeos, conjuntos de amostras, conjuntos hierárquicos de amostras, conjuntos de rotação, conjuntos bidimensionais de rotação, conjuntos de páginas e ativos de vídeo. Cada item de conjunto de mídia também pode conter uma amostra opcional. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de vídeos </p></td> 
  <td class="stentry"> <p>Um conjunto de itens que consiste em uma lista de vídeos simples. </p></td> 
 </tr> 
</table>

## Detecção de tipo de conjunto externo {#section-3dd6e453528d46898e559d31458a59ba}

Quando uma solicitação `req=set` é recebida, o tipo de resposta a ser gerada é determinado pelo valor de `catalog::AssetType`. Se `catalog::AssetType` não estiver definido, o tipo de resposta será determinado pelas seguintes regras:

* Se o registro for encontrado no catálogo de imagens E `catalog::ImageSet` for definido

   * Considere o conjunto de e-catálogos se pelo menos uma entrada no campo Registrar conjunto de imagens contiver dois pontos
   * Suponha que a mídia seja definida se pelo menos uma entrada no campo Gravar Imageset contiver dois pontos-e-vírgulas.
   * Considere o conjunto de imagens se pelo menos uma entrada no campo Gravar conjunto de imagens contiver um ponto-e-vírgula.
   * Considere o conjunto de rotação se nenhuma entrada contiver dois pontos ou ponto-e-vírgula, mas pelo menos uma entrada contiver um conjunto referenciado ou um conjunto em linha (este é um conjunto de rotação 2D).
   * Considere um conjunto desconhecido se nenhuma entrada contiver dois pontos, ponto-e-vírgula ou conjunto referenciado ou conjunto em linha (isto é, lista de imagens separada por vírgulas).

* Se o registro for encontrado em catálogos de imagem E conteúdo estático

   * Considere o vídeo se a extensão do arquivo estiver no seguinte conjunto: mp3, mp4, flv, f4v, swf, xml
   * Caso contrário, considere a imagem

* Se o registro for encontrado no catálogo de conteúdo estático, mas NÃO no catálogo de imagens

   * Considere o vídeo se a extensão do arquivo estiver no seguinte conjunto: mp3, mp4, flv, f4v, swf, xml
   * Considere estático caso contrário

* Se o registro for encontrado no catálogo de imagens, mas NÃO no catálogo de conteúdo estático

   * Assumir imagem

* Se o registro NÃO for encontrado no catálogo de imagens e NÃO for encontrado no catálogo de conteúdo estático

   * Suponha vídeo baseado em arquivo se a extensão de arquivo estiver no seguinte conjunto: mp3, mp4, flv, f4v, swf, xml
   * Caso contrário, considere a imagem baseada em arquivo

Em todos os casos, a resposta xml resultante estará em conformidade com o documento XML especificado com o nó raiz definido correspondente ao tipo detectado.

## Detecção de tipo de conjunto interno {#section-8f46490e467247e69ce284704def06f3}

Quando o conjunto externo for detectado como conjunto de mídia de tipo, a resposta conterá um conjunto de itens de conjunto de mídia correspondente a cada entrada de conjunto de mídia em `catalog::ImageSet`. Se o parâmetro de tipo opcional for especificado para uma entrada de conjunto de mídia específica, ele será mapeado para um tipo de saída de acordo com a seguinte tabela:

| Tipo de entrada | Tipo de saída |
|---|---|
| `img` | `img` |
| `basic` | `img` |
| `advanced_image` | `img` |
| `img_set` | `img_set` |
| `advanced_image_set` | `img_set` |
| `advanced_swatchset` | `img_set` |
| `spin` | `spin` |
| `video` | `video` |
| `video_set` | `video_set` |
| `static` | `static` |
| `ecat` | `ecat` |

Se o parâmetro de tipo opcional para uma entrada de conjunto de mídia específica não for especificado ou corresponder a um tipo não suportado, o tipo de item de conjunto de mídia será detectado automaticamente usando as mesmas regras que foram aplicadas no nível de conjunto externo.

## Especificação XML {#section-c1bd60948ef545759a16885bb6fcc607}

A resposta xml retornada está em conformidade com a seguinte especificação:

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

O modificador `labelkey=` é usado junto com o campo `catalog::UserData`para gerar rótulos para imagens e amostras. O campo `catalog:UserData` é analisado como um conjunto de pares de chave/valor e a chave de trabalho indexa nesse conjunto para recuperar o valor da chave fornecida. Esse valor é retornado no atributo *`l`* para *`s`* e *`i`*.

## Restrições forçadas {#section-b9f042873bee45a5ae11b69fd42f2bca}

Para limitar o tamanho da resposta e evitar problemas autorreferenciais, a profundidade máxima de aninhamento é controlada pela propriedade do servidor `PS::fvctx.nestingLimit`. Se esse limite for excedido, um erro será retornado.

Para limitar o tamanho das respostas xml para grandes conjuntos de catálogo eletrônico, os metadados privados são suprimidos para itens de conjunto de folhetos de acordo com a propriedade do servidor `PS::fvctx.brochureLimit`. Todos os metadados privados associados ao folheto serão exportados até que o limite do folheto seja atingido. Quando o limite for excedido, os mapas privados e os dados do usuário serão suprimidos e um sinalizador correspondente será definido para indicar que tipo de dados foi suprimido.

Não há suporte para conjuntos de mídia aninhados. Um conjunto de mídia aninhado é definido como um conjunto de mídia que contém um item de conjunto de mídia do tipo conjunto de mídia. Se essa condição for detectada, um erro será retornado.

## Exemplos {#section-588c9d33aa05482c86cd2b1936887228}

Para obter exemplos de respostas XML para a solicitação `req=set`, consulte a página Propriedades no cabeçalho Exemplos HTML.

`http://crc.scene7.com/is-docs/examples/properties.htm`

## Consulte também {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3),  [catálogo::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), Referência do catálogo  [de imagens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)

