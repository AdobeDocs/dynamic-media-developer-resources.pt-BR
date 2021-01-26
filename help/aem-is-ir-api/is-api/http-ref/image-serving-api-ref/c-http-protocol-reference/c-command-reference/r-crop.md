---
description: Recortar imagem. Especifica uma região de corte retangular, expressa em pixels ou normalizada em relação à imagem de origem de resolução total ou à imagem de máscara.
seo-description: Recortar imagem. Especifica uma região de corte retangular, expressa em pixels ou normalizada em relação à imagem de origem de resolução total ou à imagem de máscara.
seo-title: cultura
solution: Experience Manager
title: cultura
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c8eca467-7564-48a6-82d7-17f68a1399e1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---


# cortar{#crop}

Recortar imagem. Especifica uma região de corte retangular, expressa em pixels ou normalizada em relação à imagem de origem de resolução total ou à imagem de máscara.

`crop= *``*, *`cordsize`*`

`cropN= *``*, *`cordNsizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cabo</span></span> </p> </td> 
  <td class="stentry"> <p>O deslocamento de pixel do canto superior esquerdo da imagem de origem para o canto superior esquerdo do retângulo de corte (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cordN</span></span> </p> </td> 
  <td class="stentry"> <p>Deslocamento normalizado da parte superior esquerda da imagem de origem para a parte superior esquerda do retângulo de recorte (real, real). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> tamanho</span></span> </p></td> 
  <td class="stentry"> <p>Tamanho do recorte de corte em pixels (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>Tamanho normalizado do retângulo de corte em relação ao tamanho da imagem de origem (real, real). </p></td> 
 </tr> 
</table>

Também pode ser usado para estender a imagem além de seus limites especificando valores x, y e/ou largura negativos, valores de altura maiores que a largura e altura da imagem. Nesse caso, a área estendida é totalmente transparente (a menos que `bgColor=` seja especificado).

## Propriedades {#section-632e0405bb9940679b5f8b1c10e0902e}

Atributo imagem/máscara de origem. Aplica-se à imagem de origem da camada 0 se `layer=comp`. Ignoradas por camadas que não estão associadas a uma imagem ou máscara de origem.

## Padrão {#section-41f62d386c664f77952bc22e7286bb88}

Imagem inteira ( `cropN=0,0,1,1`).

## Exemplos {#section-2c99b481c0a04321979a3b522aa295d1}

**Recorte 10% da esquerda e 10% da direita:**

`…&cropN=0.1,0,0.8,1&…`

**Recorte 20% da borda inferior de uma imagem:**

`…&cropN=0,0,1,0.8&…`

## Consulte também {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [chapterPathbgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) ,  [âncora=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c),  [estender=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
