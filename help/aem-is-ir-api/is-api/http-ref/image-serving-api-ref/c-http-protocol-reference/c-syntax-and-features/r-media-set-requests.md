---
description: O Servidor de imagens fornece um mecanismo para buscar uma resposta de texto hierárquica (xml ou json) que representa todos os recursos e metadados associados ao ImageSet de catálogo para um registro específico.
solution: Experience Manager
title: Solicitações de conjunto de mídia
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 71efed33-6248-4d23-ab4e-2caec3449171
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '956'
ht-degree: 0%

---

# Solicitações de conjunto de mídia{#media-set-requests}

O Servidor de imagens fornece um mecanismo para buscar uma resposta de texto hierárquica (xml ou json) que representa todos os recursos e metadados associados a catalog::ImageSet de um registro específico.

Os visualizadores podem usar esse mecanismo para gerar respostas para informar a apresentação de imagens, vídeos, conjuntos de vídeos, conjuntos de amostras, conjuntos de rotação, conjuntos de páginas (catálogos eletrônicos) e conjuntos de mídia simples.

## Sintaxe da solicitação {#section-d72b1d95e4ce4bb1b332ce096c2b99f1}

O conjunto de respostas para uma `catalog::ImageSet` pode ser recuperado usando o `req=set` modificador e fazendo referência à id de registro de catálogo no caminho de rede. Como alternativa, o conjunto de imagens pode ser especificado diretamente no URL usando o `imageset=` modificador. Se a variável `imageset=` Se o modificador for usado para especificar o imageset, o valor inteiro deverá ser delimitado por chaves para escapar do valor do conjunto de imagens e garantir que qualquer modificador incluído não seja interpretado como parte da cadeia de caracteres de consulta do URL.

## Tipos de respostas definidas {#section-93eb0a1f70344da2a888e56372ad3896}

O mecanismo de definição é compatível com os seguintes tipos de respostas:

<table id="simpletable_3718A93699F64805A41BC8A24D7962D2"> 
 <tr class="strow"> 
  <td class="stentry"> <p>imagens simples </p></td> 
  <td class="stentry"> <p>Um registro de imagem sem <span class="codeph"> catalog::ImageSet</span> definido. </p></td> 
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
  <td class="stentry"> <p>Um conjunto de itens que consiste em imagens simples, conjuntos de vídeos, conjuntos de amostras, conjuntos de amostras hierárquicos, conjuntos de amostras, conjuntos de rotação bidimensionais, conjuntos de páginas e ativos de vídeo. Cada item do conjunto de mídia também pode conter uma amostra opcional. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>conjuntos de vídeos </p></td> 
  <td class="stentry"> <p>Um conjunto de itens que consiste em uma lista de vídeos simples. </p></td> 
 </tr> 
</table>

## Detecção de tipo de conjunto externo {#section-3dd6e453528d46898e559d31458a59ba}

Quando um `req=set` for recebida, o tipo de resposta a ser gerada será determinado pelo valor de `catalog::AssetType`. Se `catalog::AssetType` não estiver definido, o tipo de resposta será determinado pelas seguintes regras:

* Se o registro for encontrado no catálogo de imagens AND `catalog::ImageSet` está definido

   * Assumir o conjunto de e-catalog se pelo menos uma entrada no campo Registrar Imageset contiver dois pontos
   * Suponha que a mídia esteja definida se pelo menos uma entrada no campo Conjunto de imagens contiver dois pontos e vírgulas.
   * Suponha que a imagem esteja definida se pelo menos uma entrada no campo Registrar Conjunto de Imagens contiver um ponto e vírgula.
   * Considere o conjunto de rotação se nenhuma entrada contiver dois pontos ou ponto e vírgula, mas pelo menos uma entrada contiver um conjunto referenciado ou um conjunto em linha (esse é um conjunto de rotação 2D).
   * Considere o conjunto desconhecido se nenhuma entrada contiver dois pontos, ponto e vírgula, ou o conjunto referenciado ou o conjunto em linha (ou seja, lista de imagens separada por vírgulas).

* Se o registro for encontrado nos catálogos de imagem E conteúdo estático

   * Assume o vídeo se a extensão de arquivo estiver no seguinte conjunto: mp3, mp4, flv, f4v, swf, xml
   * Supor imagem de outra forma

* Se o registro for encontrado no catálogo de conteúdo estático, mas NÃO no catálogo de imagens

   * Assume o vídeo se a extensão de arquivo estiver no seguinte conjunto: mp3, mp4, flv, f4v, swf, xml
   * Assumir estática caso contrário

* Se o registro for encontrado no catálogo de imagens, mas NÃO no catálogo de conteúdo estático

   * Assumir imagem

* Se o registro NÃO for encontrado no catálogo de imagens e NÃO for encontrado no catálogo de conteúdo estático

   * Assumir vídeo baseado em arquivo se a extensão de arquivo estiver no seguinte conjunto: mp3, mp4, flv, f4v, swf, xml
   * Assumir imagem baseada em arquivo de outra forma

Em todos os casos, a resposta xml resultante está em conformidade com o documento XML especificado com o nó raiz definido correspondente ao tipo detectado.

## Detecção de tipo de conjunto interno {#section-8f46490e467247e69ce284704def06f3}

Quando o conjunto externo é detectado como um conjunto de mídias do tipo, a resposta contém um conjunto de itens do conjunto de mídias correspondentes a cada entrada do conjunto de mídias no `catalog::ImageSet`. Se o parâmetro de tipo opcional for especificado para uma determinada entrada do conjunto de mídia, ele será mapeado para um tipo de saída de acordo com a tabela a seguir:

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

Se o parâmetro de tipo opcional para uma determinada entrada do conjunto de mídia não for especificado ou corresponder a um tipo sem suporte, o tipo de item do conjunto de mídia será detectado automaticamente usando as mesmas regras aplicadas no nível do conjunto de mídia.

## Especificação XML {#section-c1bd60948ef545759a16885bb6fcc607}

A resposta xml retornada está em conformidade com a seguinte especificação:

`http://crc.scene7.com/is-docs/examples/mediaset.dtd`

## LabelKey {#section-bf565de6f7294cf89620343c9071f415}

A variável `labelkey=` o modificador é usado junto com o `catalog::UserData`para gerar rótulos para imagens e amostras. A variável `catalog:UserData` O campo é analisado como um conjunto de pares de chave/valor e os índices labelkey no para esse conjunto, a fim de recuperar o valor da chave fornecida. Esse valor é retornado na variável *`l`* atributo para o *`s`* e *`i`*.

## Restrições impostas {#section-b9f042873bee45a5ae11b69fd42f2bca}

Para limitar o tamanho da resposta e evitar problemas de autorreferência, a profundidade máxima de aninhamento é controlada pela propriedade do servidor `PS::fvctx.nestingLimit`. Se esse limite for excedido, um erro será retornado.

Para limitar o tamanho das respostas xml para grandes conjuntos de catálogos eletrônicos, os metadados privados são suprimidos para itens de conjunto de folhetos de acordo com a propriedade do servidor `PS::fvctx.brochureLimit`. Todos os metadados privados associados ao folheto são exportados até que o limite do folheto seja atingido. Quando o limite é excedido, os mapas privados e os dados do usuário são suprimidos, e um sinalizador correspondente é definido para indicar que tipo de dados foi suprimido.

Não há suporte para conjuntos de mídia aninhados. Um conjunto de mídia aninhado é definido como um conjunto de mídia que contém um item de conjunto de mídia do tipo conjunto de mídia. Se essa condição for detectada, um erro será retornado.

## Exemplos {#section-588c9d33aa05482c86cd2b1936887228}

Para respostas XML de exemplo para `req=set` solicitação, consulte a página Propriedades no cabeçalho Exemplos de HTML.

`http://crc.scene7.com/is-docs/examples/properties.htm`

## Consulte também {#section-625ec466c948476e800dc0c52a4532d3}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [imageset=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-imageset-req.md#reference-c42935490db84830b31e9e649895dee3), [catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [Referência do catálogo de imagens](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)
