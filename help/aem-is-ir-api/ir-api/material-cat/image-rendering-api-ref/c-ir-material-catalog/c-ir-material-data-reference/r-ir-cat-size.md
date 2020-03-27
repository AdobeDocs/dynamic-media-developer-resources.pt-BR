---
description: Tamanho da declaração. Largura, altura e espessura de um objeto de material decal.
seo-description: Tamanho da declaração. Largura, altura e espessura de um objeto de material decal.
seo-title: Tamanho
solution: Experience Manager
title: Tamanho
topic: Scene7 Image Serving - Image Rendering API
uuid: 07d41f71-e18d-4559-afc7-75dc1c45be93
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Tamanho{#size}

Tamanho da declaração. Largura, altura e espessura de um objeto de material decal.

## Propriedades {#section-967bf1112eec4032a91ed0c8a7b10a07}

Três números reais separados por vírgulas. Não pode ser negativo. Defina os valores não utilizados como 0. Podem ser omitidos zeros de rastreamento.

Especifique a largura e a altura somente se a imagem deve ser esticada para se ajustar ao tamanho especificado (a proporção pode mudar). Defina a largura ou a altura para dimensionar a imagem proporcionalmente. Defina a largura e a altura como 0 para usar `catalog::Resolution`para determinar o tamanho do objeto.

Forneça um valor de espessura para adicionar uma sombra projetada ao objeto decal. Opcional para materiais de decalque, ignorados por todos os outros materiais.

## Padrão {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Isso indica que o tamanho da decal deve ser determinado com base no catálogo::Resolution e que o objeto não tem uma espessura (portanto, nenhuma sombra será renderizada).

## Exemplos {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>O decal é forçado a 12x3 polegadas de tamanho e não tem espessura (isto é, nenhuma sombra projetada). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>O decal tem 5 polegadas de largura, a altura é determinada pela proporção da imagem e uma sombra projetada é renderizada com base em uma espessura de 1 polegada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>A largura e a altura do decal são determinadas pelo catálogo::Resolution e têm ½ polegada de espessura. </p></td> 
 </tr> 
</table>

## Consulte também {#section-31a164e781d14e92bd9d379d3c329e92}

[catálogo::Resolução](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
