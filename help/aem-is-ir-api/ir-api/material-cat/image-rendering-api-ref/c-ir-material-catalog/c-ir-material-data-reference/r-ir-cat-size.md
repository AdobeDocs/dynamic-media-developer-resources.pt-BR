---
title: Tamanho
description: Tamanho do decalque. Largura, altura e espessura de um objeto de material de decalque.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 964cb4c1-5256-40eb-94ea-761916174b79
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 1%

---

# Tamanho{#size}

Tamanho do decalque. Largura, altura e espessura de um objeto de material de decalque.

## Propriedades {#section-967bf1112eec4032a91ed0c8a7b10a07}

Três números reais separados por vírgulas. Não deve ser negativo. Defina os valores não utilizados como 0. Zeros à direita podem ser omitidos.

Especifique a largura e a altura somente se a imagem precisar ser esticada para se ajustar ao tamanho especificado (a proporção pode mudar). Defina largura ou altura para dimensionar a imagem proporcionalmente. Defina a largura e a altura como 0 para usar `catalog::Resolution`para determinar o tamanho do objeto.

Forneça um valor de espessura para adicionar uma sombra projetada ao objeto de decalque. Opcional para materiais de decalque, ignorado por todos os outros materiais.

## Padrão {#section-8029fe4dcbd1427db94a4fef1ccbbfd0}

0,0,0. Isso indica que o tamanho do decalque deve ser determinado com base em catalog::Resolution, e que o objeto não tem uma espessura (portanto, nenhuma sombra projetada é renderizada).

## Exemplos {#section-7e7166ec9a1e4f4cb026de3342fcddc3}

<table id="simpletable_E3503BD975F342C58DDB4C2B56BF0CEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>12,3 </p></td> 
  <td class="stentry"> <p>O decalque é forçado a 12x3 polegadas de tamanho e não tem espessura (isto é, sem sombra). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,5,1 </p></td> 
  <td class="stentry"> <p>O decalque tem 5 polegadas de largura, a altura é determinada pela proporção da imagem e uma sombra é renderizada com base em uma espessura de 1 polegada. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>0,0,.5 </p></td> 
  <td class="stentry"> <p>A largura e a altura do decalque são determinadas pelo catálogo::Resolution, e que tem meia polegada de espessura. </p></td> 
 </tr> 
</table>

## Consulte também {#section-31a164e781d14e92bd9d379d3c329e92}

[catálogo::Resolução](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-resolution.md#reference-09fe14e6bfbf4db6b7f4369fffecc806)
