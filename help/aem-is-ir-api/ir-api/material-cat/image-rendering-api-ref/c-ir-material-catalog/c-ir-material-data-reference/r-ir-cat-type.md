---
description: Tipo de material. Tipo de superfície do material. Usado em conjunto com o glossário de catálogo e a Rigidez do catálogo para controlar os efeitos de renderização da reflexão 3D.
solution: Experience Manager
title: Tipo
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 14%

---


# Tipo{#type}

Tipo de material. Tipo de superfície do material. Usado em conjunto com catalog::Glossário e catálogo::Rigidez para controlar efeitos de renderização de reflexo 3D.

## Propriedades {#section-86e8bc194f764c848e0ee55630a5ac1b}

Enum. Opcional para todos os materiais. Ignorado se a vinheta não tiver nenhum recurso de renderização de reflexo 3D.

<table id="simpletable_85BF61871CAA420B92B855AAB8FACA2C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Desconhecido, o servidor usa o padrão . </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Outros. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Madeira natural. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Metais polidos. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Metais escovados. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Metais antiquados. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>6 </p> </td> 
  <td class="stentry"> <p>Tinta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>7 </p> </td> 
  <td class="stentry"> <p>Enamel/Lacquer. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>8 </p> </td> 
  <td class="stentry"> <p>Papel de parede. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>9 </p> </td> 
  <td class="stentry"> <p>Plástico. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>10º </p> </td> 
  <td class="stentry"> <p>Superfície sólida. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>11º </p> </td> 
  <td class="stentry"> <p>Laminato. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>12º </p> </td> 
  <td class="stentry"> <p>Vinil. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>13º </p> </td> 
  <td class="stentry"> <p>Cerâmica. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>14. </p> </td> 
  <td class="stentry"> <p>Pedra natural. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>15. </p> </td> 
  <td class="stentry"> <p>Vidro. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>16º </p> </td> 
  <td class="stentry"> <p>Espelho. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>17º </p> </td> 
  <td class="stentry"> <p>Malha. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>18º </p> </td> 
  <td class="stentry"> <p>Roupa de porco. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>19º </p> </td> 
  <td class="stentry"> <p>Carpete. </p> </td> 
 </tr> 
</table>

## Padrão {#section-247f73b22cb846b7b7d7cc6e8af949ca}

0; o servidor determinará um padrão adequado com base em outros atributos de material.

## Consulte também {#section-a51850093b7140e683a0f8b07845843c}

[catálogo::Brilho](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb) ,  [catálogo::Rigidez](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99),  [tipo=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35)
