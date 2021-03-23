---
description: Imagem da camada.
seo-description: Imagem da camada.
seo-title: src
solution: Experience Manager
title: src
uuid: b4396848-b992-4371-a8ae-4ff1781ae1be
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---


# src{#src}

Imagem da camada.

` src= *``*|{[is|ir|fxg]'{' *`objectnestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> objeto  </span> </p> </td> 
  <td class="stentry"> <p>Objeto de imagem. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> anestedRequest  </span> </p> </td> 
  <td class="stentry"> <p>Serviço de imagem aninhado, Renderização de imagem ou solicitação externa. </p> </td> 
 </tr> 
</table>

## Descrição {#section-59ec6dc2afcb43efb34dbb0f7733543f}

Especifica a imagem de origem para uma camada de imagem.

*`object`* pode ser uma entrada de catálogo ou um arquivo image/SVG.

Consulte [objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

As solicitações aninhadas ou incorporadas são fechadas por chaves. Coloque o prefixo `is` em uma solicitação incorporada de Exibição de imagem com `ir` e em uma solicitação de renderização de gráficos FXG com `fxg`. Uma solicitação para um servidor externo é assumida se nenhum prefixo for especificado.

Consulte [Aninhamento de solicitação e Incorporação](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## Propriedades {#section-2c22bb89a35d470f833df8ba898efd93}

Atributo de camada. Aplica-se a `layer=0` se `layer=comp`. Mutuamente exclusiva com `text=` e `textPs=` na mesma camada; a última ocorrência de `text=`, `textPs=` ou `src=` prevalece e determina se esta é uma imagem ou uma camada de texto. Ignorado por camadas de efeito.

*`object`*pode não resolver para outro registro de catálogo que inclua um comando `src=` ou `mask=` em seu `catalog::Modifier`. (Use o aninhamento de solicitação para obter um efeito semelhante.)

Os prefixos `is`, `ir` e `fxg` fazem distinção entre maiúsculas e minúsculas.

## Padrão {#section-a92f3882041b4d43ae2caf014647165f}

Para a camada 0, o objeto do componente de caminho do URL é usado se `src=` não for especificado. Nenhum valor padrão para outras camadas.

## Consulte também {#section-e467e03330564796932ac081f1c9c1d0}

[catálogo::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) ,  [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f),  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0),  [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e),  [Solicitar aninhamento e incorporação](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
