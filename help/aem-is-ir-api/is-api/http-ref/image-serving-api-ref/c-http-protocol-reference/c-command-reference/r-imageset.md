---
description: Conjunto de imagens. Especifica um valor de conjunto de imagens a ser usado ao gerar resposta req=set.
seo-description: Conjunto de imagens. Especifica um valor de conjunto de imagens a ser usado ao gerar resposta req=set.
seo-title: imageSet
solution: Experience Manager
title: imageSet
uuid: ecfb3905-e3ef-4ab8-a2c4-2c3f200e0f0f
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# imageSet{#imageset}

Conjunto de imagens. Especifica um valor de conjunto de imagens a ser usado ao gerar resposta req=set.

`imageSet=val`

<table id="simpletable_F697691D166C407D82233664814F4663"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>Sequência de caracteres do conjunto de imagens. </p></td> 
 </tr> 
</table>

Para escapar do valor e garantir que todos os modificadores incluídos não sejam interpretados como parte da string de consulta de URL, o valor inteiro deve ser inserido em chaves. Se o registro do catálogo for especificado no caminho de rede, esse valor do modificador substituirá `catalog::ImageSet` do registro principal. Para obter uma descrição da sintaxe de conjunto de imagens válida, consulte a documentação `catalog::ImageSet` .

## Propriedades {#section-66e7bb7bf4664cbcac6f7ebb2f0d3a4f}

Atributo da solicitação. Opcional. Substitui `catalog::ImageSet` do registro principal.

## Padrão {#section-e8622ff40408450fb79d028f8d37fa6b}

Nenhum.

## Exemplo {#section-68513d3c601f477399602a0741dab390}

Especifique o conjunto de imagens para usar com a solicitação `req=set`:

`http://server/myRootId?imageSet={asset1,asset2,asset3}&req=set`

## Consulte também {#section-7e0320b2e09d475897082711a8f023a9}

[catálogo::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md) ,  [req=set](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), Solicitações do conjunto de  [mídia](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-media-set-requests.md#reference-f2f2aa11208b47609fe17848d3b86a0b)
