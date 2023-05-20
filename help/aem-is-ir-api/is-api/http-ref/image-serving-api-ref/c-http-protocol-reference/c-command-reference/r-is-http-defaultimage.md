---
description: Imagem de resposta padrão. Especifica a entrada de imagem ou catálogo a ser usada quando uma imagem não for encontrada.
solution: Experience Manager
title: defaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 741833b5-e858-4aa5-96c1-bb06539deef3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# defaultImage{#defaultimage}

Imagem de resposta padrão. Especifica a entrada de imagem ou catálogo a ser usada quando uma imagem não for encontrada.

` defaultImage= *`objeto`*`

<table id="simpletable_C1FC14B7D9AE476DB2B10EB402944335"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> objeto </span> </span> </p> </td> 
  <td class="stentry"> <p>Objeto de imagem. </p> </td> 
 </tr> 
</table>

*`object`* pode ser uma entrada de catálogo (incluindo um modelo) ou um caminho de arquivo de imagem simples. Útil para substituir imagens ausentes por imagens padrão. Esse valor substitui o valor do catálogo correspondente `attribute::DefaultImage`. Um valor vazio ( `defaultImage=`) desativa a manipulação de imagem padrão.

>[!NOTE]
>
>O mecanismo de imagem padrão não se aplica a objetos SVG. Um erro será retornado se o objeto SVG especificado na solicitação não for encontrado.

Se `attribute::DefaultImageMode=0`, *`object`* substitui toda a solicitação original, mesmo se apenas uma imagem em uma composição de várias imagens estiver ausente. Os únicos comandos retidos da solicitação original são: `wid=`, `hei=`, `fmt=`, `qlt=`.

Se `attribute::DefaultImageMode=1`, o objeto substitui somente a imagem de camada ausente; os atributos da camada ausente são aplicados e o composto é processado e retornado normalmente.

## Propriedades {#section-d30923d8dc4042eba10989212dd70887}

Solicitar atributo. Aplica-se independentemente da configuração da camada atual. Ignorado se `req=` é diferente de `img` ou `tmb`.

## Restrições {#section-30df31bc8cac41cd917f1e45196779c2}

As fontes de imagem estrangeiras não são cobertas pelo mecanismo de imagem padrão; um erro é retornado se uma fonte de imagem estrangeira não for válida.

O Servidor de imagens é revertido para `DefaultImageMode=0` quando as solicitações aninhadas de Renderização de Imagem ou renderização FXG falham.

## Padrão {#section-0676c66b233c46a3a3a1517da4ace998}

`attribute::DefaultImage`.

## Consulte também {#section-745392143c3747a2955e1ae561f58e5f}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [attribute:: DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [ *`object`* ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)
