---
description: Opções de arquivo PostScript.
seo-description: Opções de arquivo PostScript.
seo-title: PostScriptOptions
solution: Experience Manager
title: PostScriptOptions
topic: Dynamic Media Image Production System API
uuid: 31526bfe-b651-47a8-98c0-2750a3d9cabf
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# PostScriptOptions{#postscriptoptions}

Opções de arquivo PostScript.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`processo`*` | `xsd:string` | Opção de processo PostScript. |
| `*`resolução`*` | `xsd:double` | Resolução do arquivo. |
| `*`colorspace`*` | `xsd:string` | Modo de espaço de cores PostScript. |
| `*`alfa`*` | `xsd:boolean` | Se o arquivo deve ser rasterizado em uma imagem. Em caso afirmativo, criará um plano de fundo transparente se o arquivo original for definido dessa forma. Geralmente usado para criar logotipos sobrepostos. |
| `*`extractSearchWords`*` | `xsd:boolean` | Se as palavras de pesquisa devem ser extraídas do arquivo PostScript. |

