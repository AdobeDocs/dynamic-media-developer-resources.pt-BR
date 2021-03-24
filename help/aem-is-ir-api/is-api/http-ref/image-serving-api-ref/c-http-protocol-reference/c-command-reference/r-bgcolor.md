---
description: Cor do Plano de Fundo da Camada. Especifica a cor de plano de fundo e a opacidade da camada atual.
solution: Experience Manager
title: bgColor
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# bgColor{#bgcolor}

Cor do Plano de Fundo da Camada. Especifica a cor de plano de fundo e a opacidade da camada atual.

`bgColor= *`color`*`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span></span> </p> </td> 
  <td class="stentry"> <p>Valor de cor cinza, RGB ou CMYK, com ou sem alfa. </p></td> 
 </tr> 
</table>

Áreas transparentes e semiopacas dentro do retângulo delimitador da camada são preenchidas com a cor especificada* após* `opac=`, `rotate=` e `extend=` serem aplicadas.

## Propriedades {#section-19dfc13e997f4a33889a1df1e4ad50b9}

Atributo de camada. Aplica-se à camada atual ou à camada 0 se `layer=comp`. Ignorado por camadas de efeito.

*`color`* presume-se que existe no espaço de cores de trabalho correspondente ao tipo de pixel de  *`color`*. *`color`* é convertida com precisão se a imagem da camada final tiver um tipo de pixel diferente.

## Padrão {#section-30cd43f922c04ed9b75875ff7f20c88f}

0,0,0,0 (totalmente transparente).

## Exemplo {#section-6e14fcf1d31e432dbdb56b9320904453}

Consulte [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423).

## Consulte também {#section-64b3f153c6d94ab58f46e77324697818}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93),  [color=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-color-commandref.md#reference-b044954ec6184253b8831579466b4423),  [blendMode=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172),  [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5),  [estender=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac),  [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096),  [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88),  [Gerenciamento de cores](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
