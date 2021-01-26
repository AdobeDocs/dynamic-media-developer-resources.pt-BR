---
description: Atributos de texto no caminho.
seo-description: Atributos de texto no caminho.
seo-title: pathAttr
solution: Experience Manager
title: pathAttr
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b0ca5821-ee08-4c18-919d-775b75f19acd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# pathAttr{#pathattr}

Atributos de texto no caminho.

` pathAttr= *``*[, *``*[, *`directionstartPosendPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> direção  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norma  </span> |  <span class="codeph"> reverso  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos  </span> </p> </td> 
  <td class="stentry"> <p>Posição do start de texto no caminho (real 0.0...1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos  </span> </p> </td> 
  <td class="stentry"> <p>Posição final do texto no caminho (real 0.0..&lt;2.0). </p> </td> 
 </tr> 
</table>

Especifique `norm` para desenhar o texto que começa perto do primeiro vértice de caminho e `reverse` para desenhar o texto na direção oposta, começando perto do último vértice.

*`startPos`* e  *`endPos`* permitir o ajuste do local em que o texto será desenhado no caminho. 0,0 corresponde ao primeiro vértice do caminho e 1,0 ao último vértice; os valores intermediários expressam a distância ao longo do caminho entre o primeiro e o último vértice.

## Propriedades {#section-80f266da4e2549d89f022a3f9ff4584d}

Atributo de camada. Ignorado se a camada não incluir os comandos `textPs=` e `textPath=`.

*`startPos`* deve ser maior ou igual a 0 e menor que 1,0.  *`endPos`* deve ser maior  *`startPos`* e menor ou igual a 1,0 quando aplicado a um caminho aberto, ou menor ou igual a (  *`startPos`* + 1,0) quando aplicado a um caminho fechado.

## Padrão {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Consulte também {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) ,  [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
