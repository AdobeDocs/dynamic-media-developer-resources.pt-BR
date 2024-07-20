---
description: Opções de arquivo do PostScript.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

Opções de arquivo do PostScript.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| processo | `xsd:string` | Opção de processo do PostScript. |
| resolution | `xsd:double` | Resolução do arquivo. |
| colorspace | `xsd:string` | Modo de espaço de cores do PostScript. |
| alfa | `xsd:boolean` | Se o arquivo deve ser rasterizado em uma imagem. Nesse caso, ele criará um plano de fundo transparente se o arquivo original for definido dessa maneira. Geralmente usado para criar logotipos de sobreposição. |
| extractSearchWords | `xsd:boolean` | Se as palavras de pesquisa devem ser extraídas do arquivo PostScript. |
