---
description: Nitidez. Atributo de nitidez, determina quando o material é nitidez durante o processamento.
solution: Experience Manager
title: Nítido
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce08ed97-33b7-4d28-8f7f-3f3ef8598ad6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 3%

---

# Nítido{#sharp}

Nitidez. Atributo de nitidez, determina quando o material é nitidez durante o processamento.

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
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Mais nitidez (antes e depois da transformação). </p></td> 
 </tr> 
</table>

Ignorado por materiais de cor sólida, opcional para todos os outros materiais.

## Padrão {#section-a6bc204d552b4cc3ae6a77ec232c26ff}

`attribute::Sharpening` é usado se o campo não estiver presente, se estiver vazio ou se o valor não for uma das opções com suporte.

## Consulte também {#section-b462f9ad9ae347e1a1993abf2f2daa8e}

[attribute::Sharpening](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-cat-sharp.md#reference-c706450cf95347f98f86c696f9167297) , [catalog::RenderSettings](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rendersettings.md#reference-f3ae5e18095d40b2a8edef957dd82fbd), [sharp=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a)
