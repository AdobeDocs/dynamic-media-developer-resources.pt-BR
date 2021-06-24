---
description: Opções de arquivo PostScript.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '72'
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
