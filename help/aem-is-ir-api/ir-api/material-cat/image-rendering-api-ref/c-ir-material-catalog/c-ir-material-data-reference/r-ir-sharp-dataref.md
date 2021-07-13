---
description: Nitidez. O atributo de nitidez determina quando o material é aprimorado durante a renderização.
solution: Experience Manager
title: Nitidez
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: ce08ed97-33b7-4d28-8f7f-3f3ef8598ad6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 3%

---

# Nitidez{#sharp}

Nitidez. O atributo de nitidez determina quando o material é aprimorado durante a renderização.

O tipo e a quantidade de nitidez são controlados pela vinheta por meio de um modelo de material padrão ou com `catalog::RenderSettings`.

## Propriedades {#section-aac81b1a611b4bca90b8544eae7896df}

Enum.

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Sem nitidez. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Nitidez normal (após a transformação). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Nitidez alternativa (antes da transformação). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Mais nitidez (antes e depois da transformação). </p></td> 
 </tr> 
</table>

Ignorado por materiais de cor sólida, facultativo para todos os outros materiais.

## Padrão {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` é usado se o campo não estiver presente, se estiver vazio ou se o valor não for uma das opções suportadas.

## Consulte também {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[atributo::Nitidez](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) ,  [catálogo::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd),  [nítido=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
