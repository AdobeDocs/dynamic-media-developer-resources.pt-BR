---
title: tamanho
description: Tamanho do decalque. Especifica o tamanho de um material de decalque.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 756d8b9f-076a-48d6-95c9-e0d6caeed3dd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 0%

---

# tamanho{#size}

Tamanho do decalque. Especifica o tamanho de um material de decalque.

` size= *`largura,altura`*[ *`,espessura`*]`

<table id="simpletable_00B1226F3B8B49D895D1269AB03D5043"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> largura, altura </span> </p> </td> 
  <td class="stentry"> <p>Tamanho do objeto de decalque em unidades de coordenadas de cena (normalmente polegadas) (real, real). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> espessura </span> </p> </td> 
  <td class="stentry"> <p>Espessura do objeto de decalque em unidades de coordenadas de cena (normalmente polegadas) (real). </p> </td> 
 </tr> 
</table>

Se nem a largura nem a altura forem 0, a imagem será dimensionada com as dimensões exatas especificadas e a proporção da imagem não será preservada. A configuração de qualquer valor como 0 preserva a proporção da imagem.

Se *`thickness`* for especificado, uma sombra será renderizada se o objeto de vinheta definir um vetor de luz apropriado. Defina *`thickness`* como 0 para desabilitar a renderização de sombra projetada.

## Propriedades {#section-818e01e91fed4015951189c818ef28d8}

Atributo de material. Usado apenas por decalques; ignorado por todos os outros materiais. `res=` será ignorado se a largura ou a altura forem maiores que 0. Os valores não devem ser negativos.

## Padrão {#section-f91f516c6af54f0eb4d8c964b923cae0}

`catalog::Size` se o material de decalque for baseado em uma entrada de catálogo; caso contrário, `size=0,0,0`. O tamanho do decalque é calculado a partir de `res=` se *`wid`* e *`hei`* não estiverem especificados ou estiverem definidos como 0. Nenhuma sombra projetada será renderizada se *`thickness`* não for especificado ou se estiver definido como 0.

## Exemplo {#section-04fdc2b60b9e4071b672bf6a913738ad}

Um MSS para um decalque, que é dimensionado com base na resolução, girado em 20 graus no sentido horário, e tem uma espessura de 2,5 polegadas, para um efeito de sombra de gota apropriado:

`…&decal&src=myDecal.png&res=34&rotate=20&size=0,0,2.5&…`

## Consulte também {#section-1b116ecd60214732a1757ee1f0cf21c2}

[Coordenadas de Cena](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-vignettes/c-ir-scene-coordinates.md#concept-528507024fa640b19a2631357febf7f1), [res=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04), [attribute::Resolution](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
