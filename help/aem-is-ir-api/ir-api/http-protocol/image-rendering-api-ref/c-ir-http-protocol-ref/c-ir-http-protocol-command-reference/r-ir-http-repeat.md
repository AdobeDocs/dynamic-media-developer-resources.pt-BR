---
description: Modo de repetição de textura. Especifica o modo de repetição para materiais de textura repetíveis.
seo-description: Modo de repetição de textura. Especifica o modo de repetição para materiais de textura repetíveis.
seo-title: repetição
solution: Experience Manager
title: repetição
topic: Scene7 Image Serving - Image Rendering API
uuid: 6508fdff-27cd-4038-b506-39b927f3526a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# repetição{#repeat}

Modo de repetição de textura. Especifica o modo de repetição para materiais de textura repetíveis.

`repeat=0...19`

<table id="simpletable_0D54E62EAF50482A95EDE166D0645D9E"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Repetição direta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Lado a lado aleatório de 4 vias. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Ocasionamento aleatório de 8 vias. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Lado a lado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>O papel de parede pendurado no quarto lugar. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>O papel de parede pendurado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p> </td> 
  <td class="stentry"> <p>Suspensão de papel de parede. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p> </td> 
  <td class="stentry"> <p>Suspensão do papel de parede da 5ª gota. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p> </td> 
  <td class="stentry"> <p>Suspensão inversa do papel de parede. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p> </td> 
  <td class="stentry"> <p>Papel de parede aleatório pendurado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p> </td> 
  <td class="stentry"> <p>Queda aleatória. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p> </td> 
  <td class="stentry"> <p>De maneira aleatória. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p> </td> 
  <td class="stentry"> <p>Metade do outro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p> </td> 
  <td class="stentry"> <p>Espelho (correspondência). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p> </td> 
  <td class="stentry"> <p>Aleatório padrão. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p> </td> 
  <td class="stentry"> <p>Aleatório de alta frequência. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p> </td> 
  <td class="stentry"> <p>Aleatório de baixa frequência. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p> </td> 
  <td class="stentry"> <p>Aleatório horizontal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p> </td> 
  <td class="stentry"> <p>Aleatório vertical. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p> </td> 
  <td class="stentry"> <p>Aresta aleatória. </p> </td> 
 </tr> 
</table>

Os modos de coloração aleatória (14.1.18) podem ser utilizados para sintetizar texturas a partir de imagens que não possam ser repetidas facilmente; o algoritmo criará texturas totalmente aleatórias ou parcialmente aleatórias com base na imagem original.

## Propriedades {#section-262bf540930d4890b678ea00cefe1909}

Atributo material. Ignorados por materiais de cor sólida, decalque e gabinete.

## Padrão {#section-e5bbd7d9fbb74852849e605d20f550bb}

`catalog::Repeat`, se o material for baseado em uma entrada de catálogo, caso contrário `0` (repetição direta).

## Consulte também {#section-ac99113b64654d75a3a86e41db546269}

[catálogo::Repetir](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-repeat.md#reference-20e149211e1f4e8285db5ecb83c1902e)
