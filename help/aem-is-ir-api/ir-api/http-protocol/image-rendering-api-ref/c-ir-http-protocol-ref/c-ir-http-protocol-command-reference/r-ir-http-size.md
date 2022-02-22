---
title: size
description: Tamanho Decal. Especifica o tamanho de um material de decalque.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---

# size{#size}

Tamanho Decal. Especifica o tamanho de um material de decalque.

` size= *`largura,altura`*[ *`,espessura`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> largura, altura </span> </p> </td> 
  <td class="stentry"> <p>Tamanho do objeto decalque em unidades de coordenadas de cena (tipicamente polegadas) (real, real). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> thickness </span> </p> </td> 
  <td class="stentry"> <p>Espessura do objeto do decalque em unidades de coordenadas de cena (tipicamente polegadas) (real). </p> </td> 
 </tr> 
</table>

Se nenhuma largura ou altura for 0, a imagem será dimensionada para as dimensões exatas especificadas e a proporção da imagem não será preservada. Definir um dos valores como 0 preserva a proporção da imagem.

If *`thickness`* for especificada, uma sombra será renderizada se o objeto da vinheta definir um vetor de luz adequado. Definir *`thickness`* como 0 para desativar a renderização de sombra.

## Propriedades {#section-818e01e91fed4015951189c818ef28d8}

Atributo de material. Utilizado apenas por decalques; ignoradas por todos os outros materiais. `res=` é ignorada se a largura ou a altura forem maiores que 0. Os valores não devem ser negativos.

## Padrão {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` se o material de declaração se basear numa entrada de catálogo; otherwise `size=0,0,0`. O tamanho da decalque é calculado a partir de `res=` if *`wid`* e *`hei`* não são especificados ou estão definidos como 0. Nenhuma sombra será renderizada se *`thickness`* não foi especificado ou definido como 0.

## Exemplo {#section-04fdc2b60b9e4071b672bf6a913738ad}

Um MSS para um decalque, dimensionado com base na resolução, rodado 20 graus no sentido horário e com uma espessura de 2,5 polegadas, para um efeito de sombra apropriado:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Consulte também {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Coordenadas de Cena](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04), [atributo::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
