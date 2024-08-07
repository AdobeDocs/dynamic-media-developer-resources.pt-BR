---
title: texto
description: Texto de camada. Especifica o texto e o conteúdo de formatação de uma camada de texto.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3966b180-bef1-4fad-af71-ba42bbdffd59
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 0%

---

# texto{#text}

Texto de camada. Especifica o texto e o conteúdo de formatação de uma camada de texto.

` text= *`cadeia de caracteres`*`

<table id="simpletable_6C095D7F69874A8EA3D1D52103FA520C"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> cadeia de caracteres </span> </p> </td> 
  <td class="stentry"> <p>String RTF (Rich Text Formatted - Formatado em Rich Text) ou string de texto sem formatação. </p> </td> 
 </tr> 
</table>

Todo o controle de formatação de fonte, cor de fonte e parágrafo é obtido com comandos RTF. Consulte [Formatação do Texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) para obter mais informações.

`text=` oferece suporte ao dimensionamento automático do texto para preencher o retângulo de camada especificado com `size=`.

Consulte [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d).

`text=` dá suporte ao dimensionamento automático da camada de texto para ajustar-se ao texto renderizado (quando `size=` não é especificado ou quando apenas a largura é especificada). Observe que, nesse caso, somente um dos comandos de alinhamento RTF `\ql`, `\qr` e `\qc` pode ser aplicado; caso contrário, um erro será retornado.

## Propriedades {#section-8c0f020094a44c6b858454ef91ab4edf}

Atributo de camada. Aplica-se a `layer=0` se `layer=comp`. Mutualmente exclusivo com `src=` e `textPs=` na mesma camada; a última ocorrência de `text=`, `textPs=` e `src=` prevalece e determina se esta é uma imagem ou uma camada de texto. Ignorado pelas camadas de efeito.

## Padrão {#section-58958671e0ad479e8d5f6c1d41d7dc74}

Nenhum.

## Exemplo {#section-d011f765ec5c418d814a821019b0eef0}

Veja os exemplos em [Formatação do Texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c) e [Exemplo A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) em [Modelos](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consulte também {#section-207b779ab67342a5acd343e6bcc749c4}

[Formatação do Texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/c-text-formatting.md#concept-0d3136db7f6f49668274541cd4b6364c), [Posicionamento do Texto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-positioning.md#reference-f647443d92914f4b89a7cc5a83267d87), [src=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [textPs=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textps.md#reference-4209a2a6169f44278da2647cfb0cd767)
