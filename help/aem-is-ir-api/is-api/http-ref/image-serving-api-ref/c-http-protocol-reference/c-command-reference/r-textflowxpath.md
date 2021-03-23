---
description: Área de exclusão do fluxo de texto. Especifica uma ou mais regiões a serem excluídas do fluxo de texto.
seo-description: Área de exclusão do fluxo de texto. Especifica uma ou mais regiões a serem excluídas do fluxo de texto.
seo-title: textFlowXPath
solution: Experience Manager
title: textFlowXPath
uuid: ce833ae7-e774-4954-a521-b6247e75f6eb
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---


# textFlowXPath{#textflowxpath}

Área de exclusão do fluxo de texto. Especifica uma ou mais regiões a serem excluídas do fluxo de texto.

`textFlowXPath= *`pathDefinition`*`

<table id="simpletable_7E0EA48AEBB5426CBE948FCA18882C66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Dados do caminho. </p></td> 
 </tr> 
</table>

Consulte [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obter informações adicionais, incluindo uma descrição de *`pathDefinition`*. Se nenhuma definição de caminho for especificada, `textFlowXPath=` será ignorada.

## Propriedades {#section-cd1ebb151d4a405fbfc508d46522d686}

Atributo da camada de texto (somente `textPs=`). Ignorado por outras camadas ou quando especificado sem `textFlowPath=`. Aplica-se a `layer=0` se especificado para `layer=comp`.

## Padrão {#section-9405cda904684d829ed12a9e40a4dc46}

Nenhum.

## Consulte também {#section-855228e744c7437a921d5db5b24bcd95}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef)
