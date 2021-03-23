---
description: Tamanho Decal. Especifica o tamanho de um material de decalque.
seo-description: Tamanho Decal. Especifica o tamanho de um material de decalque.
seo-title: size
solution: Experience Manager
title: size
uuid: b82f3429-3d84-4707-8126-d390239df9a2
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 0%

---


# size{#size}

Tamanho Decal. Especifica o tamanho de um material de decalque.

` size= *`largura,altura`*[ *`,espessura`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> largura, altura  </span> </p> </td> 
  <td class="stentry"> <p>Tamanho do objeto decalque em unidades de coordenadas de cena (tipicamente polegadas) (real, real). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> thickness  </span> </p> </td> 
  <td class="stentry"> <p>Espessura do objeto do decalque em unidades de coordenadas de cena (tipicamente polegadas) (real). </p> </td> 
 </tr> 
</table>

Se nem a largura nem a altura forem 0, a imagem será dimensionada para as dimensões exatas especificadas e a proporção da imagem não será preservada. Definir um dos valores como 0 preserva a proporção da imagem.

Se *`thickness`* for especificado, uma sombra será renderizada se o objeto de vinheta definir um vetor de luz adequado. Defina *`thickness`* como 0 para desativar a renderização de sombra.

## Propriedades {#section-818e01e91fed4015951189c818ef28d8}

Atributo de material. Utilizado apenas por decalques; ignoradas por todos os outros materiais. `res=` é ignorada se a largura ou a altura forem maiores que 0. Os valores não devem ser negativos.

## Padrão {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` se o material de declaração se basear numa entrada de catálogo; caso contrário  `size=0,0,0`. O tamanho da decalque é calculado a partir de `res=` se *`wid`* e *`hei`* não estiverem especificadas ou estiverem definidas como 0. Nenhuma sombra é renderizada se *`thickness`* não for especificado ou definido como 0.

## Exemplo {#section-04fdc2b60b9e4071b672bf6a913738ad}

Um MSS para um decalque, dimensionado com base na resolução, rodado 20 graus no sentido horário e com uma espessura de 2,5 polegadas, para um efeito de sombra apropriado:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Consulte também {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Coordenadas](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1) da Cena,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04),  [atributo::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
