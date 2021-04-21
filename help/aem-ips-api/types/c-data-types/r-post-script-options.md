---
description: Opções de arquivo PostScript.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---


# PostScriptOptions{#postscriptoptions}

Opções de arquivo PostScript.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`processo`*` | `xsd:string` | Opção de processo PostScript. |
| `*`resolution`*` | `xsd:double` | Resolução de arquivo. |
| `*`colorspace`*` | `xsd:string` | Modo de espaço de cores PostScript. |
| `*`alfa`*` | `xsd:boolean` | Se o arquivo deve ser rasterizado em uma imagem. Em caso afirmativo, ele criará um plano de fundo transparente se o arquivo original estiver definido dessa maneira. Geralmente usado para criar logotipos sobrepostos. |
| `*`extractSearchWords`*` | `xsd:boolean` | Extrair palavras de pesquisa do arquivo PostScript. |

