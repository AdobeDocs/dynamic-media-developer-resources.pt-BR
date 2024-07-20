---
title: src
description: Imagem de camada.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 88b89e70-59cf-4fb9-bbe7-0ac5eff792f1
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# src{#src}

Imagem de camada.

` src= *`object`*|{[is|ir|fxg]'{' *`nestedRequest`*'}'}`

<table id="simpletable_59104309B8284B21ABCE7DC95BF5A273"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> objeto </span> </p> </td> 
  <td class="stentry"> <p>Objeto de imagem. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> nestedRequest </span> </p> </td> 
  <td class="stentry"> <p>Servidor de imagens aninhado, Renderização de imagens ou solicitação externa. </p> </td> 
 </tr> 
</table>

## Descrição {#section-59ec6dc2afcb43efb34dbb0f7733543f}

Especifica a imagem de origem de uma camada de imagem.

*`object`* pode ser uma entrada de catálogo ou um arquivo de imagem/SVG.

Consulte [objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

As solicitações aninhadas ou incorporadas são colocadas entre chaves. Prefixe uma solicitação de Servidor de Imagens incorporada com `is`, uma solicitação de Renderização de Imagens incorporada com `ir` e uma solicitação de renderização de gráficos FXG com `fxg`. Uma solicitação para um servidor externo será presumida se nenhum prefixo for especificado.

Consulte [Aninhamento e incorporação de solicitação](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b).

## Propriedades {#section-2c22bb89a35d470f833df8ba898efd93}

Atributo de camada. Aplica-se a `layer=0` se `layer=comp`. Mutualmente exclusivo com `text=` e `textPs=` na mesma camada; a última ocorrência de `text=`, `textPs=` ou `src=` prevalece e determina se esta é uma imagem ou uma camada de texto. Ignorado pelas camadas de efeito.

*`object`*pode não resolver para outro registro de catálogo que inclui um comando `src=` ou `mask=` em seu `catalog::Modifier`. (Use o aninhamento de solicitações para obter um efeito semelhante.)

Os prefixos `is`, `ir` e `fxg` diferenciam maiúsculas de minúsculas.

## Padrão {#section-a92f3882041b4d43ae2caf014647165f}

Para a camada 0, o objeto do componente de caminho da URL será usado se `src=` não for especificado. Nenhum valor padrão para outras camadas.

## Consulte também {#section-e467e03330564796932ac081f1c9c1d0}

[catálogo::Caminho](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [texto=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [máscara=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Solicitar Aninhamento e Incorporação](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-request-nesting-and-embedding.md#reference-38ec66d4062046589e16c39bf1c6049b)
