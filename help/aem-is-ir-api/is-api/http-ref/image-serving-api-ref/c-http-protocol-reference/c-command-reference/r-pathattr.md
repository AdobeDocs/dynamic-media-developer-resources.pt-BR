---
title: pathAttr
description: Atributos de texto no caminho.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fdf9274a-70d0-4692-a7a9-c108abb9ab84
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# pathAttr{#pathattr}

Atributos de texto no caminho.

` pathAttr= *`direção`*[, *`startPos`*[, *`endPos`*]]`

<table id="simpletable_EC76095316AF4F07B1DDCC0D72B814CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> direção </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> norma </span> | <span class="codeph"> reverter </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> startPos </span> </p> </td> 
  <td class="stentry"> <p>Posição inicial do texto no caminho (real 0.0...1.0). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> endPos </span> </p> </td> 
  <td class="stentry"> <p>Posição final do texto no caminho (real 0,0...&lt;2,0). </p> </td> 
 </tr> 
</table>

Especificar `norm` para desenhar o texto começando próximo ao primeiro vértice do caminho e `reverse` para desenhar o texto na direção oposta, começando perto do último vértice.

*`startPos`* e *`endPos`* permite ajustar onde o texto é desenhado no demarcador. 0,0 corresponde ao primeiro vértice no caminho e 1,0 ao último vértice; valores intermediários expressam a distância ao longo do caminho entre o primeiro e o último vértice.

## Propriedades {#section-80f266da4e2549d89f022a3f9ff4584d}

Atributo de camada. Ignorado se a camada não incluir `textPs=` e `textPath=` comandos.

*`startPos`* deve ser maior ou igual a 0 e menor que 1,0. *`endPos`* deve ser maior que *`startPos`* e menor ou igual a 1.0 quando aplicado a um caminho aberto, ou menor ou igual a ( *`startPos`* + 1.0) quando aplicado a um caminho fechado.

## Padrão {#section-3e757970885c45e7b6100e78dc08626f}

`pathAttr=norm,0,1`

## Consulte também {#section-b869745de1da4ef996dfda4af39ed14d}

[textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd) , [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
