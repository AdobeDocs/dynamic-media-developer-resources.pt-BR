---
title: modelo
description: Modelo de composição. Permite especificar um modelo de composição localizado em um catálogo diferente do catálogo principal.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 56ebf2a1-f2c3-4b3f-8d0a-9383f1411440
TQID: 'https://experienceleague.adobe.com/O1v1LorIfXLyRso4ZRVJd7qx5A4kciWKVoG-df8q-Xg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 166
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

Quando `template=` está presente, o objeto especificado no caminho da solicitação não é aplicado como a origem da camada 0. No entanto, ele pode ser referenciado como um `src=` ou `mask=` em qualquer lugar no modelo usando a variável de caminho predefinida `$object$` como um valor `src=`. `catalog::Modifier` do objeto especificado no caminho da solicitação é aplicado somente com a substituição de `$object$` no modelo, enquanto `catalog::PostModifier` é sempre aplicado.

A camada 0 é definida no corpo do modelo e pode ser uma imagem, cor sólida, texto ou camada de solicitação aninhada ou incorporada.

`catalog:PostModifier` de *`object`* é ignorado quando *`object`* é usado com `template=`.

## Padrão {#section-9de53ea27c4b4fd4811e40e345d8ba05}

Nenhum.

## Propriedades {#section-daf3afb1d09c45a6a394468d0874c439}

Solicitar atributo. Aplica-se independentemente da configuração da camada atual.

## Exemplo {#section-9a4f260ed43342b186b0fe855f34bca6}

Veja os exemplos em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consulte também {#section-067587444f774469931ecafd5a39834c}

[objeto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e), [Variável de Caminho Predefinida](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-is-http-substitution-variables.md#reference-90dc01aba44940e4acdd0c6476e7aa5a)
