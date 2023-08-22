---
title: imageSet
description: Conjunto de imagens. Especifica um valor de conjunto de imagens a ser usado ao gerar a resposta req=set.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 318c658d-7126-40f6-870b-11294a3f6f5f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# imageSet{#imageset}

Conjunto de imagens. Especifica um valor de conjunto de imagens a ser usado ao gerar a resposta req=set.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Sequência de caracteres do conjunto de imagens. </p></td> 
 </tr> 
</table>

Para escapar o valor e garantir que qualquer modificador incluído não seja interpretado como parte da string de consulta do URL, o valor inteiro deve ser delimitado por chaves. Se o registro do catálogo for especificado no caminho líquido, esse valor do modificador substituirá `catalog::ImageSet` do registro principal. Para obter uma descrição de sintaxe de conjunto de imagens válida, consulte `catalog::ImageSet` documentação.

## Propriedades {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

Solicitar atributo. Opcional. Substituições `catalog::ImageSet` do registro principal.

## Padrão {#section-e8622ff40408450fb79d028f8d37fa6b}

Nenhum.

## Exemplo {#section-68513d3c601f477399602a0741dab390}

Especificar conjunto de imagens para uso com `req=set` solicitação:

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## Consulte também {#section-7e0320b2e09d475897082711a8f023a9}

[catalog::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) , [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Solicitações de conjunto de mdias](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
