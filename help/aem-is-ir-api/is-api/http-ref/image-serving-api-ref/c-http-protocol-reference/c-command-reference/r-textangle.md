---
title: textAngle
description: Direção de renderização do texto. Especifica o ângulo no qual o texto especificado com textPs= é apresentado e renderizado na caixa de texto (definido com size= ou textFlowPath=).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 102dbdc0-77b8-4c60-b456-6cf693e0b38b
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---

# textAngle{#textangle}

Direção de renderização do texto. Especifica o ângulo no qual o texto especificado com textPs= é apresentado e renderizado na caixa de texto (definido com size= ou textFlowPath=).

` textAngle= *`ângulo`*`

<table id="simpletable_40832AC4B43A458CA69B225768124F58"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> ângulo </span> </p> </td> 
  <td class="stentry"> <p>Ângulo de direção (graus). </p> </td> 
 </tr> 
</table>

Valores positivos giram o texto no sentido horário; `textAngle=90` desenha o texto de cima para baixo.

## Propriedades {#section-6d586a632daa4261a8ce62db56140b36}

Atributo de camada. Aplica-se a `layer=0` se `layer=comp`. Ignorado se `textPs=` não for especificado para esta camada ou se `textPath=` for especificado.

## Padrão {#section-49a9f5819c994c27928282c14b2bb2a7}

`textAngle=0` para nenhuma rotação.

## Consulte também {#section-dccc29ff33704061b2519b56b7be45fd}

[Formatação do Texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [Posicionamento do Texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd)
