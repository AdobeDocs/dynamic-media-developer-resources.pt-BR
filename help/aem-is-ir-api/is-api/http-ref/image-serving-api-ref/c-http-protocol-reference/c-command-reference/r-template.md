---
description: Modelo de composição. Permite especificar um modelo de composição localizado em um catálogo diferente do catálogo principal.
solution: Experience Manager
title: modelo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---

# modelo{#template}

Modelo de composição. Permite especificar um modelo de composição em um catálogo diferente do catálogo principal.

`template= *`modelo`*`

<table id="simpletable_DEC6F4EB460D453B8F272C98C9C8B7E5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> objeto</span> </p> </td> 
  <td class="stentry"> <p>Modelo. </p></td> 
 </tr> 
</table>

*`template`* deve ser uma entrada do catálogo de imagens com o corpo do modelo contido em `catalog::Modifier`.

Quando `template=` estiver presente, o objeto especificado no caminho da solicitação não será aplicado como origem da camada 0. No entanto, pode ser referido como um `src=` ou `mask=` em qualquer lugar no modelo usando a variável de caminho predefinida `$object$` as a `src=` valor. `catalog::Modifier` do objeto especificado no caminho da solicitação é aplicado somente com a substituição de `$object$` no modelo, enquanto `catalog::PostModifier` é sempre aplicado.

A camada 0 é definida no corpo do modelo e pode ser uma imagem, cor sólida, texto ou camada de solicitação aninhada ou incorporada.

`catalog:PostModifier` de *`object`* é ignorado quando *`object`* é usado com `template=`.

## Padrão {#section-9de53ea27c4b4fd4811e40e345d8ba05}

Nenhum.

## Propriedades {#section-daf3afb1d09c45a6a394468d0874c439}

Solicitar atributo. Aplica-se independentemente da configuração da camada atual.

## Exemplo {#section-9a4f260ed43342b186b0fe855f34bca6}

Veja os exemplos em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consulte também {#section-067587444f774469931ecafd5a39834c}

[objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Variável de caminho predefinida](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
