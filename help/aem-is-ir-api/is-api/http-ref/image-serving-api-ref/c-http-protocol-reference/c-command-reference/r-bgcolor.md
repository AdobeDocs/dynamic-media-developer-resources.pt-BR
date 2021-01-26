---
description: Cor do plano de fundo da camada. Especifica a cor e a opacidade do plano de fundo da camada atual.
seo-description: Cor do plano de fundo da camada. Especifica a cor e a opacidade do plano de fundo da camada atual.
seo-title: bgColor
solution: Experience Manager
title: bgColor
topic: Dynamic Media Image Serving - Image Rendering API
uuid: bcbd368f-d200-4b1f-8e9f-bf4d88f14b72
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 0%

---


# bgColor{#bgcolor}

Cor do plano de fundo da camada. Especifica a cor e a opacidade do plano de fundo da camada atual.

`bgColor= *`cor`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cor</span></span> </p> </td> 
  <td class="stentry"> <p>Valor de cor cinza, RGB ou CMYK, com ou sem alfa. </p></td> 
 </tr> 
</table>

As áreas transparentes e semiopacas dentro do retângulo delimitador da camada são preenchidas com a cor especificada* após a aplicação de* `opac=`, `rotate=` e `extend=`.

## Propriedades {#section-19dfc13e997f4a33889a1df1e4ad50b9}

Atributo de camada. Aplica-se à camada atual ou à camada 0 se `layer=comp`. Ignorado pelas camadas de efeito.

*`color`* presume-se que existe no espaço de cor de trabalho correspondente ao tipo de pixel de  *`color`*. *`color`* é convertida com precisão se a imagem da camada final tiver um tipo de pixel diferente.

## Padrão {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0 (totalmente transparente).

## Exemplo {#section-6e14fcf1d31e432dbdb56b9320904453}

Consulte [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423).

## Consulte também {#section-64b3f153c6d94ab58f46e77324697818}

[cor](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [cor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423),  [modoMesclagem=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172),  [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5),  [estender=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)  [ ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88)  [girar=, bgc=, gerenciamento de cores,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
