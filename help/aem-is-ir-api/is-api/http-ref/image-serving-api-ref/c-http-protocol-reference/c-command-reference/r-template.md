---
description: Modelo de composição. Permite especificar um modelo de composição localizado em um catálogo diferente do catálogo principal.
seo-description: Modelo de composição. Permite especificar um modelo de composição localizado em um catálogo diferente do catálogo principal.
seo-title: template
solution: Experience Manager
title: template
topic: Scene7 Image Serving - Image Rendering API
uuid: 59b37d60-1d0c-4d0b-a5a0-98d8bf9e9064
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# template{#template}

Modelo de composição. Permite especificar um modelo de composição localizado em um catálogo diferente do catálogo principal.

`template= *`template`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> objeto</span> </p> </td> 
  <td class="stentry"> <p>Modelo. </p></td> 
 </tr> 
</table>

*`template`* deve ser uma entrada do catálogo de imagens com o corpo do modelo contido em `catalog::Modifier`.

Quando `template=` estiver presente, o objeto especificado no caminho da solicitação não será aplicado como a origem da camada 0, mas poderá ser referenciado como um `src=` ou `mask=` em qualquer lugar no modelo usando a variável de caminho predefinida `$object$` como um `src=` valor. `catalog::Modifier` do objeto especificado no caminho da solicitação é aplicado somente em conexão com a substituição de `$object$` dentro do modelo, enquanto `catalog::PostModifier` é sempre aplicado.

A camada 0 é definida no corpo do modelo e pode ser uma imagem, cor sólida, texto ou camada de solicitação aninhada ou incorporada.

`catalog:PostModifier` for *`object`* ignorada quando *`object`* for usada com `template=`.

## Padrão {#section-9de53ea27c4b4fd4811e40e345d8ba05}

Nenhum.

## Propriedades {#section-daf3afb1d09c45a6a394468d0874c439}

Atributo de solicitação. Aplica-se independentemente da configuração de camada atual.

## Example {#section-9a4f260ed43342b186b0fe855f34bca6}

Consulte os exemplos em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consulte também {#section-067587444f774469931ecafd5a39834c}

[objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), Variável de caminho [predefinida](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
