---
description: Alinhamento de renderização de textura. Especifica qual dos pontos de origem definidos pelo objeto de vinheta selecionado deve ser usado.
seo-description: Alinhamento de renderização de textura. Especifica qual dos pontos de origem definidos pelo objeto de vinheta selecionado deve ser usado.
seo-title: alinhar
solution: Experience Manager
title: alinhar
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 0b24cd82-f9b2-48f4-9052-8c2026370ff7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 2%

---


# alinhar{#align}

Alinhamento de renderização de textura. Especifica qual dos pontos de origem definidos pelo objeto de vinheta selecionado deve ser usado.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Origem padrão (correspondência central). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Origem de correspondência contínua. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Alinhamento aleatório. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3,6 </p></td> 
  <td class="stentry"> <p>Origem definida pelo usuário. </p></td> 
 </tr> 
</table>

O renderizador aplica a textura ao objeto para que o ponto de ancoragem da textura ( `anchor=`) coincida com o ponto de origem especificado.

Cada objeto pode definir até 6 pontos de origem (0,1, 3, 4, 5, 6). Se um valor `align` for especificado, mas o ponto de origem correspondente não for definido pelo objeto de vinheta, o ponto de origem padrão (correspondência central) será usado.

`align=2` especifica o alinhamento aleatório de textura, caso em que  `anchor=` é efetivamente ignorado.

Usada principalmente para materiais estofados, possivelmente para tecidos de vestuário, para gerenciar o alinhamento da textura entre objetos adjacentes.

## Propriedades {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Atributo material. Ignorado se um objeto de quadro de revestimento de parede, gabinete, equipamento ou janela estiver selecionado ou se o material não for uma textura repetível.

## Padrão {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, se o material for baseado em uma entrada de catálogo, caso contrário, 0 (correspondido no centro).

## Consulte também {#section-945d1ce275df487d9d564d4043156c79}

[catálogo::Alinhamento](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) ,  [âncora=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
