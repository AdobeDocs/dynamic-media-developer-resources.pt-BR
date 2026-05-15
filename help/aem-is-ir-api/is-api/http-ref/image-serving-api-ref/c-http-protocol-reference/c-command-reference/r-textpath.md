---
title: textPath
description: Caminho do texto. Especifica o caminho a ser usado como a linha de base para o texto fornecido com textPs=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1c515786-bbba-44d3-837e-b474af293b7e
TQID: 'https://experienceleague.adobe.com/zVKtDOaScVXM-69CquAw4cpc81Wj7X47LLxBf0RdJ6c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 0%

---

# textPath{#textpath}

Caminho do texto. Especifica o caminho a ser usado como a linha de base para o texto fornecido com textPs=.

textPath= *`pathDefinition`*

<table id="simpletable_74F549E8625B483A9B334B24A7EB6D22"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> pathDefinition</span> </p> </td> 
  <td class="stentry"> <p>Dados de caminho. </p></td> 
 </tr> 
</table>

Consulte [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) para obter informações adicionais, incluindo uma descrição de *`pathDefinition`*.

>[!NOTE]
>
>Diferente de `clipPath=`, caminhos de texto não são fechados automaticamente quando &#39;z&#39; ou &#39;Z&#39; não são especificados no final de um subcaminho.

*`pathDefinition`* pode incluir vários subcaminhos. O texto é renderizado nos subcaminhos na ordem especificada.

Os comandos RTF `\ql`, `\qc`, `\qr`, `\li` e `\ri` podem ser usados para posicionar o texto renderizado ao longo do caminho.

## Propriedades {#section-068137df436c46b9b55d271eb60e7285}

Atributo de camada de texto (somente `textPs=`). Ignorado por outras camadas. Aplicável a `layer=0`, se especificado, para `layer=comp`. Ignorado se `textPs=` estiverem presentes.

Um erro será retornado se uma camada incluir `textPath=` e `textFlowPath=`.

## Padrão {#section-697b1f2cfc43498080a31327e6eb173d}

Nenhum, para renderização de texto padrão.

## Consulte também {#section-3050d8f47e1d4f5c9b474dece45ea93d}

[textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767) , [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [Camadas de Texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
