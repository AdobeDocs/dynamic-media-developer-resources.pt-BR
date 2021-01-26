---
description: Tipo de superfície do material. Especifica o tipo de superfície do material.
seo-description: Tipo de superfície do material. Especifica o tipo de superfície do material.
seo-title: type
solution: Experience Manager
title: type
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0f107d50-b363-4670-bb02-873677e7bbea
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 11%

---


# type{#type}

Tipo de superfície do material. Especifica o tipo de superfície do material.

`type=0...19`

<table id="simpletable_482728CD58144E7BBB2912B2F105FDCA"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Desconhecido, o servidor usa o padrão </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Outros </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Madeira natural </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Metal polido </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p></td> 
  <td class="stentry"> <p>Metal escovado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p></td> 
  <td class="stentry"> <p>Metal Antiquado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p></td> 
  <td class="stentry"> <p>Tinta </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p></td> 
  <td class="stentry"> <p>Enamel/Lacquer </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p></td> 
  <td class="stentry"> <p>Wallpaper </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p></td> 
  <td class="stentry"> <p>Plástico </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10 </p></td> 
  <td class="stentry"> <p>Superfície sólida </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11 </p></td> 
  <td class="stentry"> <p>Laminato </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12 </p></td> 
  <td class="stentry"> <p>Vinil </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13 </p></td> 
  <td class="stentry"> <p>Cerâmica </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14 </p></td> 
  <td class="stentry"> <p>Pedra natural </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15 </p></td> 
  <td class="stentry"> <p>Vidro </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16 </p></td> 
  <td class="stentry"> <p>Espelho </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17 </p></td> 
  <td class="stentry"> <p>Malha </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18 </p></td> 
  <td class="stentry"> <p>Sheer Fabric </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19 </p></td> 
  <td class="stentry"> <p>Carpete </p></td> 
 </tr> 
</table>

Usado em conjunto com `gloss=` e `rough=` para controlar os comportamentos de reflexo e efeito de brilho. Materiais diferentes produzirão efeitos diferentes, mesmo se `gloss=` e `rough=` forem os mesmos.

## Propriedades {#section-2345b2508273426295ce8ac46182ea64}

Atributo material. Ignorado se a vinheta não incluir dados de reflexão 3D ou se os efeitos de brilho estiverem desativados na vinheta.

## Padrão {#section-0989055fb74a41a3b2f2a47fe7d90a42}

`catalog::Type` se o material for baseado em uma entrada de catálogo. Caso contrário, `type=0`. Se não for especificado, ou se `type=0`, o servidor selecionará um padrão adequado, dependendo do objeto do público alvo e dos outros atributos de material.

## Consulte também {#section-7cf808b0bb3d4b4fbb7b9a850d5a038b}

[brilho=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) ,  [bruto=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180)
