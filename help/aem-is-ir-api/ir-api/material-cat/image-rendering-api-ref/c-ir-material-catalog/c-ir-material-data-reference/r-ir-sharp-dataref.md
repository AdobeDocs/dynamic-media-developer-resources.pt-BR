---
description: Nitidez. O atributo de nitidez determina quando o material é afiado durante a renderização.
seo-description: Nitidez. O atributo de nitidez determina quando o material é afiado durante a renderização.
seo-title: Sharp
solution: Experience Manager
title: Sharp
topic: Dynamic Media Image Serving - Image Rendering API
uuid: f153f496-f2c5-43d0-a7f0-00045fd96af8
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---


# Sharp{#sharp}

Nitidez. O atributo de nitidez determina quando o material é afiado durante a renderização.

O tipo e a quantidade de nitidez são controlados pela vinheta através de um modelo de material padrão ou com `catalog::RenderSettings`.

## Propriedades {#section-aac81b1a611b4bca90b8544eae7896df}

Enum.

<table id="simpletable_D52B41A39E4E4E54A06821B9D689DB30"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Sem nitidez. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
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

Ignorados por materiais de cor sólida, opcionais para todos os outros materiais.

## Padrão {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` é usado se o campo não estiver presente, se estiver vazio ou se o valor não for uma das opções suportadas.

## Consulte também {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[atributo::Nitidez](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) ,  [catálogo::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd),  [nítido=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
