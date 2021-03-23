---
description: Modo de repetição de textura. Especifica o modo de repetição para materiais de textura repetíveis.
seo-description: Modo de repetição de textura. Especifica o modo de repetição para materiais de textura repetíveis.
seo-title: repetição
solution: Experience Manager
title: repetição
uuid: 6508fdff-27cd-4038-b506-39b927f3526a
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 11%

---


# repetir{#repeat}

Modo de repetição de textura. Especifica o modo de repetição para materiais de textura repetíveis.

`repeat=0...19`

<table id="simpletable_0D54E62EAF50482A95EDE166D0645D9E"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Repetição direta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Otimização aleatória de 4 vias. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Otimização aleatória de 8 vias. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Lado a lado. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Suspensão do papel de parede. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Travamento do papel de parede de terceira gota. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p> </td> 
  <td class="stentry"> <p>Travamento de papel de parede com meia gota. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p> </td> 
  <td class="stentry"> <p>Suspensão do papel de parede. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p> </td> 
  <td class="stentry"> <p>Travamento inverso do papel de parede. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p> </td> 
  <td class="stentry"> <p>Suspensão aleatória de papel de parede. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10º </p> </td> 
  <td class="stentry"> <p>Queda aleatória. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11º </p> </td> 
  <td class="stentry"> <p>Aleatório. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12º </p> </td> 
  <td class="stentry"> <p>Metade da frente. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13º </p> </td> 
  <td class="stentry"> <p>Espelho (correspondência de marcadores). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14. </p> </td> 
  <td class="stentry"> <p>Aleatório padrão. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15. </p> </td> 
  <td class="stentry"> <p>Aleatório de alta frequência. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16º </p> </td> 
  <td class="stentry"> <p>Aleatório de baixa frequência. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17º </p> </td> 
  <td class="stentry"> <p>Aleatório horizontal. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18º </p> </td> 
  <td class="stentry"> <p>Aleatório vertical. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19º </p> </td> 
  <td class="stentry"> <p>Edge randomizer. </p> </td> 
 </tr> 
</table>

Os modos de colcha aleatória (14...18) podem ser utilizados para sintetizar texturas de imagens que não são facilmente repetíveis; o algoritmo criará texturas totalmente aleatórias ou parcialmente aleatórias com base na imagem original.

## Propriedades {#section-262bf540930d4890b678ea00cefe1909}

Atributo de material. Ignorado por materiais de cor sólida, decalque e armário.

## Padrão {#section-e5bbd7d9fbb74852849e605d20f550bb}

`catalog::Repeat`, se o material for baseado em uma entrada de catálogo, caso contrário  `0` (repetição direta).

## Consulte também {#section-ac99113b64654d75a3a86e41db546269}

[catálogo::Repetir](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-repeat.md#reference-20e149211e1f4e8285db5ecb83c1902e)
