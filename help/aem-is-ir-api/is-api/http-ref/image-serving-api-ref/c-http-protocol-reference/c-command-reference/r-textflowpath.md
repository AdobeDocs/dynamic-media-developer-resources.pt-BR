---
description: Área de fluxo de texto. Especifica uma ou mais regiões nas quais o texto especificado com textPs= deve ser continuado.
seo-description: Área de fluxo de texto. Especifica uma ou mais regiões nas quais o texto especificado com textPs= deve ser continuado.
seo-title: textFlowPath
solution: Experience Manager
title: textFlowPath
topic: Scene7 Image Serving - Image Rendering API
uuid: 5449d78f-e56b-4afb-a05a-7cf8f1f37278
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# textFlowPath{#textflowpath}

Área de fluxo de texto. Especifica uma ou mais regiões nas quais o texto especificado com textPs= deve ser continuado.

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition  </span> </p> </td> 
  <td class="stentry"> <p>Dados de caminho. </p> </td> 
 </tr> 
</table>

Consulte [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obter informações adicionais, incluindo uma descrição de *`pathDefinition`*.

Os comandos de margem RTF `\margl`, `\margr`, `\margt` e `\margb` são ignorados quando `textFlowPath=` está presente. Se nenhuma definição de caminho for especificada, `textFlowPath=` será ignorada.

## Propriedades {#section-b68dc887c6534ce8982cad740b3aeaa4}

Atributo de camada de texto (somente `textPs=`). Ignorado por outras camadas. Aplica-se a `layer=0` se especificado para `layer=comp`.

## Padrão {#section-68c4559b9e8242059b82e5a39a455dfc}

Igual ao retângulo da camada; o texto preenche todo o retângulo da camada.

## Consulte também {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15), Camadas  [de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
