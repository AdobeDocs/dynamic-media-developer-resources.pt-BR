---
description: Imagem de resposta padrão. Especifica a imagem ou entrada de catálogo a ser usada quando uma imagem não puder ser encontrada.
solution: Experience Manager
title: defaultImage
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# defaultImage{#defaultimage}

Imagem de resposta padrão. Especifica a imagem ou entrada de catálogo a ser usada quando uma imagem não puder ser encontrada.

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
>O mecanismo de imagem padrão não se aplica a objetos SVG. Um erro é retornado se o objeto SVG especificado na solicitação não puder ser encontrado.

Se `attribute::DefaultImageMode=0`, *`object`* substitui toda a solicitação original, mesmo se apenas uma imagem em uma composição de várias imagens estiver ausente. Os únicos comandos retidos da solicitação original são: `wid=`, `hei=`, `fmt=`, `qlt=`.

Se `attribute::DefaultImageMode=1`, o objeto substitui apenas a imagem da camada ausente; os atributos para a camada ausente são aplicados e o composto é processado e retornado como de costume.

## Propriedades {#section-d30923d8dc4042eba10989212dd70887}

Atributo da solicitação. Aplica-se independentemente da configuração de camada atual. Ignorado se `req=` for diferente de `img` ou `tmb`.

## Restrições {#section-30df31bc8cac41cd917f1e45196779c2}

As fontes de imagem estrangeiras não são abrangidas pelo mecanismo de imagem predefinido; um erro será retornado se uma fonte de imagem estrangeira não for válida.

O Serviço de imagem reverte para `DefaultImageMode=0` quando a Renderização de imagem aninhada ou as solicitações de renderização FXG falham.

## Padrão {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Consulte também {#section-745392143c3747a2955e1ae561f58e5f}

[atributo::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [atributo: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1),  [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
