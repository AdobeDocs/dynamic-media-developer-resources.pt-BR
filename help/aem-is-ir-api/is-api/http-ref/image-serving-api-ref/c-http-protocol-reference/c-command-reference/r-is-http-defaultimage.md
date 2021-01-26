---
description: Imagem de resposta padrão. Especifica a entrada de imagem ou catálogo a ser usada quando uma imagem não puder ser encontrada.
seo-description: Imagem de resposta padrão. Especifica a entrada de imagem ou catálogo a ser usada quando uma imagem não puder ser encontrada.
seo-title: defaultImage
solution: Experience Manager
title: defaultImage
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 7478325c-9ac5-4b85-a4c5-5c495f924eb5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---


# defaultImage{#defaultimage}

Imagem de resposta padrão. Especifica a entrada de imagem ou catálogo a ser usada quando uma imagem não puder ser encontrada.

` defaultImage= *`objeto`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objeto  </span> </span> </p> </td> 
  <td class="stentry"> <p>Objeto de imagem. </p> </td> 
 </tr> 
</table>

*`object`* pode ser uma entrada de catálogo (incluindo um modelo) ou um caminho de arquivo de imagem simples. Útil para substituir imagens ausentes por imagens padrão. Esse valor substitui o valor do catálogo correspondente `attribute::DefaultImage`. Um valor vazio ( `defaultImage=`) desativa o manuseio de imagem padrão.

>[!NOTE]
>
>O mecanismo de imagem padrão não se aplica a objetos SVG. Um erro será retornado se o objeto SVG especificado na solicitação não puder ser encontrado.

Se `attribute::DefaultImageMode=0`, *`object`* substituirá a solicitação original inteira, mesmo se apenas uma imagem em uma composição de várias imagens estiver ausente. Os únicos comandos retidos da solicitação original são: `wid=`, `hei=`, `fmt=`, `qlt=`.

Se `attribute::DefaultImageMode=1`, o objeto substituirá apenas a imagem de camada ausente; os atributos para a camada ausente são aplicados e a composição é processada e retornada como de costume.

## Propriedades {#section-d30923d8dc4042eba10989212dd70887}

Atributo de solicitação. Aplica-se independentemente da configuração de camada atual. Ignorado se `req=` for diferente de `img` ou `tmb`.

## Restrições {#section-30df31bc8cac41cd917f1e45196779c2}

As fontes de imagem estrangeiras não são abrangidas pelo mecanismo de imagem predefinido; um erro será retornado se uma fonte de imagem estrangeira não for válida.

O Serviço de imagem reverte para `DefaultImageMode=0` quando as solicitações de renderização de imagem aninhadas ou FXG falham.

## Padrão {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Consulte também {#section-745392143c3747a2955e1ae561f58e5f}

[atributo::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [atributo: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
