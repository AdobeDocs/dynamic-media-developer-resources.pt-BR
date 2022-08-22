---
title: alinhar
description: Alinhamento da renderização da textura. Especifica qual dos pontos de origem definidos pelo objeto de vinheta selecionado deve ser usado.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b76f173-809b-4b41-bf39-6b85f77ab2db
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 2%

---

# alinhar {#align}

Alinhamento da renderização da textura. Especifica qual dos pontos de origem definidos pelo objeto de vinheta selecionado deve ser usado.

`align=0|1|2|3|4|5|6`

<table id="simpletable_D15233999E35488EB2F933BD72798E2F"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Origem padrão (centro-correspondência). </p></td> 
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
  <td class="stentry"> <p>3.6. </p></td> 
  <td class="stentry"> <p>Origem definida pelo usuário. </p></td> 
 </tr> 
</table>

O renderizador aplica a textura ao objeto para que o ponto de ancoragem da textura ( `anchor=`) coincide com o ponto de origem especificado.

Cada objeto pode definir até seis pontos de origem (0, 1, 3, 4, 5, 6). Se uma `align` é especificado, mas o ponto de origem correspondente não é definido pelo objeto da vinheta, o ponto de origem padrão (correspondência central) é usado.

`align=2` Especifica alinhamento de textura aleatório, nesse caso `anchor=` é efetivamente ignorada.

Usada principalmente para materiais estofados, possivelmente para tecidos de vestuário, para gerenciar o alinhamento da textura entre objetos adjacentes.

## Propriedades {#section-350fadc87dcf4812a8a02d1c3d6697a0}

Atributo de material. Ignorado se for selecionado um objeto de estrutura de parede, armário, equipamento ou revestimento de janela, ou se o material não for uma textura repetível.

## Padrão {#section-3231c2854bae4477836b626ac208dd34}

`catalog::Alignment`, se o material for baseado em uma entrada de catálogo, caso contrário, 0 (correspondido no centro).

## Consulte também {#section-945d1ce275df487d9d564d4043156c79}

[catálogo::Alinhamento](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399) , [âncora=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
