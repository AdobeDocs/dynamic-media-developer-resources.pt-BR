---
description: Tamanho da declaração. Especifica o tamanho de um material decal.
seo-description: Tamanho da declaração. Especifica o tamanho de um material decal.
seo-title: tamanho
solution: Experience Manager
title: tamanho
topic: Scene7 Image Serving - Image Rendering API
uuid: b82f3429-3d84-4707-8126-d390239df9a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---


# size{#size}

Tamanho da declaração. Especifica o tamanho de um material decal.

` size= *`largura,altura`*[ *`,espessura`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> largura, altura  </span> </p> </td> 
  <td class="stentry"> <p>Tamanho do objeto decal em unidades de coordenadas de cena (tipicamente polegadas) (real, real). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> espessura  </span> </p> </td> 
  <td class="stentry"> <p>Espessura do objeto decal em unidades de coordenadas de cena (tipicamente polegadas) (real). </p> </td> 
 </tr> 
</table>

Se nem a largura nem a altura forem 0, a imagem será dimensionada para as dimensões exatas especificadas e a proporção da imagem não será preservada. Definir qualquer valor como 0 preserva a proporção da imagem.

Se *`thickness`* for especificado, uma sombra projetada será renderizada se o objeto de vinheta definir um vetor de luz adequado. Defina *`thickness`* como 0 para desativar a renderização de sombra.

## Propriedades {#section-818e01e91fed4015951189c818ef28d8}

Atributo material. Utilizados apenas por decalques; ignorados por todos os outros materiais. `res=` é ignorada se a largura ou a altura for maior que 0. Os valores não devem ser negativos.

## Padrão {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` se o material de declaração se basear numa entrada de catálogo; caso contrário  `size=0,0,0`. O tamanho da declaração é calculado a partir de `res=` se *`wid`* e *`hei`* não forem especificados ou estiverem definidos como 0. Nenhuma sombra projetada é renderizada se *`thickness`* não for especificado ou definido como 0.

## Exemplo {#section-04fdc2b60b9e4071b672bf6a913738ad}

Um MSS para um decal, que é dimensionado com base na resolução, girado 20 graus no sentido horário e tem uma espessura de 2,5 polegadas, para um efeito de sombra projetada adequado:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Consulte também {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Coordenadas](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1) de cena,  [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04),  [atributo::Resolução](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
