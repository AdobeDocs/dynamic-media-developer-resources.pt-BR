---
description: Caminho do texto. Especifica o caminho a ser usado como linha de base para o texto fornecido com textPs=.
seo-description: Caminho do texto. Especifica o caminho a ser usado como linha de base para o texto fornecido com textPs=.
seo-title: textPath
solution: Experience Manager
title: textPath
uuid: a2f0047b-ad62-4605-a723-b43d53fbea56
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Profissional de negócios
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---


# textPath{#textpath}

Caminho do texto. Especifica o caminho a ser usado como linha de base para o texto fornecido com textPs=.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Dados do caminho. </p></td> 
 </tr> 
</table>

Consulte [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obter informações adicionais, incluindo uma descrição de *`pathDefinition`*.

>[!NOTE]
>
>Diferente de `clipPath=`, os caminhos de texto não são fechados automaticamente quando &#39;z&#39; ou &#39;Z&#39; não é especificado no final de um subcaminho.

*`pathDefinition`* pode incluir vários subcaminhos. O texto é renderizado nos subcaminhos na ordem especificada.

Os comandos RTF `\ql`, `\qc`, `\qr`, `\li` e `\ri` podem ser usados para posicionar o texto renderizado ao longo do caminho.

## Propriedades {#section-068137df436c46b9b55d271eb60e7285}

Atributo da camada de texto (somente `textPs=`). Ignorado por outras camadas. Aplica-se a `layer=0` se especificado para `layer=comp`. Ignorado se `textPs=` estiver presente.

Um erro é retornado se uma camada incluir `textPath=` e `textFlowPath=`.

## Padrão {#section-697b1f2cfc43498080a31327e6eb173d}

Nenhum, para renderização de texto padrão.

## Consulte também {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) ,  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d),  [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), Camadas  [de texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
