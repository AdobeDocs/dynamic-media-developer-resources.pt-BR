---
title: textFlowXPath
description: Área de exclusão de fluxo de texto. Especifica uma ou mais regiões para excluir do fluxo de texto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2430ab43-c032-4c2f-93c3-225e8116f100
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 0%

---

# textFlowXPath{#textflowxpath}

Área de exclusão de fluxo de texto. Especifica uma ou mais regiões para excluir do fluxo de texto.

`textFlowXPath= *`definiçãoCaminho`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Dados de caminho. </p></td> 
 </tr> 
</table>

Consulte [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obter informações adicionais, incluindo uma descrição de *`pathDefinition`*. Se nenhuma definição de caminho for especificada, `textFlowXPath=` será ignorado.

## Propriedades {#section-cd1ebb151d4a405fbfc508d46522d686}

Atributo de camada de texto (somente `textPs=`). Ignorado por outras camadas ou quando especificado sem `textFlowPath=`. Aplicável a `layer=0`, se especificado, para `layer=comp`.

## Padrão {#section-9405cda904684d829ed12a9e40a4dc46}

Nenhum.

## Consulte também {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
