---
description: Área do fluxo de texto. Especifica uma ou mais regiões em que o texto especificado com textPs= deve ser continuado.
solution: Experience Manager
title: textFlowPath
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# textFlowPath{#textflowpath}

Área do fluxo de texto. Especifica uma ou mais regiões em que o texto especificado com textPs= deve ser continuado.

` textFlowPath= *`pathDefinition`*`

<table id="simpletable_52CEFF5C3CCB4642A9A320D01B1BF8E0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> pathDefinition  </span> </p> </td> 
  <td class="stentry"> <p>Dados do caminho. </p> </td> 
 </tr> 
</table>

Consulte [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obter informações adicionais, incluindo uma descrição de *`pathDefinition`*.

Os comandos de margem RTF `\margl`, `\margr`, `\margt` e `\margb` são ignorados quando `textFlowPath=` está presente. Se nenhuma definição de caminho for especificada, `textFlowPath=` será ignorada.

## Propriedades {#section-b68dc887c6534ce8982cad740b3aeaa4}

Atributo da camada de texto (somente `textPs=`). Ignorado por outras camadas. Aplica-se a `layer=0` se especificado para `layer=comp`.

## Padrão {#section-68c4559b9e8242059b82e5a39a455dfc}

Igual ao retângulo de camada; o texto preenche todo o retângulo de camada.

## Consulte também {#section-592b0039cf99471188db6a7df44b450a}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef),  [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15), Camadas  [de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
