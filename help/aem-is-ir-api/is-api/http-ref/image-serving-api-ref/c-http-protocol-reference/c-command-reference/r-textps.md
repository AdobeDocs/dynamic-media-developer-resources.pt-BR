---
title: textPs
description: Texto de camada (compatível com Adobe Photoshop). Especifica o corpo de texto para uma camada de texto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 95f343ce-bea3-425e-9a25-d1d141a976d9
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# textPs{#textps}

Texto de camada (compatível com Adobe Photoshop). Especifica o corpo de texto para uma camada de texto.

`textPs= *`cadeia de caracteres`*`

<table id="simpletable_4E2D08FD4EEC4EDC9EFE9F6F2E22DB0C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> cadeia de caracteres</span> </span> </p> </td> 
  <td class="stentry"> <p>Cadeia de caracteres em formato Rich Text (RTF). </p></td> 
 </tr> 
</table>

Todo o controle de formatação de fonte, cor de fonte e parágrafo é obtido com comandos RTF.

Consulte [Formatação do Texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c).

`textPs=` dá suporte a recursos estendidos, como justificativa, fluxo de texto em regiões não retangulares definidas com `textFlowPath=` e/ou `textFlowXPath=` e renderização de texto ao longo de caminhos arbitrários definidos com `textPath=`.

## Propriedades {#section-a289dc26b6534b41998b1e241d5f2f92}

Atributo de camada. Aplica-se a `layer=0` se `layer=comp`. Mutualmente exclusivo com `src=` e `text=` na mesma camada. A última ocorrência de `text=`, `textPs=` e `src=` prevalece e determina se esta é uma imagem ou uma camada de texto. Ignorado pelas camadas de efeito.

## Padrão {#section-11c2ae2c96d64a0a9c207252df663e4d}

Nenhum.

## Consulte também {#section-5c2b25767d2b47b5be817271ab12e13c}

[Formatação do Texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [text=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-text.md#reference-84634052e48548539a1ef63cbe41f22f), [textFlowPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowpath.md#reference-0b8d9493d71342f0b6a64a6d221584ef), [textFlowXPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textflowxpath.md#reference-c55d4e41a28f40aca6a24ca218c28542), [textPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textpath.md#reference-b09cc0902dff4725bdb54d5da4076ccd), [textAngle=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textangle.md#reference-447f624c0e764d0cb5c75846d1b44d15)
