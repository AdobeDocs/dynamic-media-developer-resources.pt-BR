---
description: Opções de arquivo PDF.
solution: Experience Manager
title: PDFOoptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---


# PDFOoptions{#pdfoptions}

Opções de arquivo PDF.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`processo`*` | `xsd:string` | Escolha de &quot;processos PDF&quot;. |
| `*`resolution`*` | `xsd:double` | Resolução de arquivo. |
| `*`colorspace`*` | `xsd:string` | Opção de Modo Colorspace Pós-script. |
| `*`pdfCatalog`*` | `xsd:boolean` | Combinar um PDF de várias páginas em um eCatalog após a renderização (o padrão é verdadeiro). |
| `*`extractSearchWords`*` | `xsd:boolean` | Se as palavras de pesquisa devem ser extraídas do arquivo PDF. |
| `*`extractLinks`*` | `xsd:boolean` | Se os links PDF devem ser extraídos em mapas de imagem atribuídos às páginas rasterizadas no IPS. |

