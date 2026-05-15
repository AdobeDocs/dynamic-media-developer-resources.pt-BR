---
title: cortar
description: Cortar imagem. Especifica uma região de corte retangular, expressa em pixels ou normalizada em relação à imagem de origem com resolução total ou imagem de máscara.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d1ea63c1-95f0-4a4e-b65d-eb535eef0205
TQID: 'https://experienceleague.adobe.com/sFmHyBwHZcqIxp9LWE8IphN3RCa-auGEph0WbFzs1n0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 0%

---

# cortar{#crop}

Cortar imagem. Especifica uma região de corte retangular, expressa em pixels ou normalizada em relação à imagem de origem com resolução total ou imagem de máscara.

`crop= *`coord`*, *`size`*`

`cropN= *`coordN`*, *`sizeN`*`

<table id="simpletable_472A9AD67AA64419B0877B0535F8B14A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span></span> </p> </td> 
  <td class="stentry"> <p>Deslocamento em pixels do canto superior esquerdo da imagem de origem para o canto superior esquerdo do recorte (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>Deslocamento normalizado da parte superior esquerda da imagem de origem para a parte superior esquerda do recorte (real, real). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> tamanho</span></span> </p></td> 
  <td class="stentry"> <p>Tamanho do corte reto em pixels (int, int). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> sizeN</span></span> </p></td> 
  <td class="stentry"> <p>Tamanho normalizado do recorte em relação ao tamanho da imagem de origem (real, real). </p></td> 
 </tr> 
</table>

Também pode ser usado para estender a imagem além de seus limites, especificando valores negativos de x, y e/ou largura, valores de altura maiores que a largura e a altura da imagem. Nesse caso, a área estendida é totalmente transparente (a menos que `bgColor=` seja especificado).

## Propriedades {#section-632e0405bb9940679b5f8b1c10e0902e}

Atributo de imagem/máscara do Source. Aplica-se à imagem de origem da camada 0 se `layer=comp`. Ignorado por camadas que não estão associadas a uma imagem ou máscara de origem.

## Padrão {#section-41f62d386c664f77952bc22e7286bb88}

Imagem inteira ( `cropN=0,0,1,1`).

## Exemplos {#section-2c99b481c0a04321979a3b522aa295d1}

**Recortar 10% da esquerda e 10% da direita:**

`…&cropN=0.1,0,0.8,1&…`

**Recortar 20% da borda inferior de uma imagem:**

`…&cropN=0,0,1,0.8&…`

## Consulte também {#section-d5616c7aa0ce4faa88f51dd5662e5daf}

[cropPath](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-croppath.md) [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac)
