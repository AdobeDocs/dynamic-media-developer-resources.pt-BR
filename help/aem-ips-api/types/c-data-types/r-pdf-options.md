---
description: Opções de arquivo PDF.
seo-description: Opções de arquivo PDF.
seo-title: PDFOoptions
solution: Experience Manager
title: PDFOoptions
topic: Dynamic Media Image Production System API
uuid: 7558b6b5-ad32-4baf-896b-f4e2bd48f2ec
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 0%

---


# PDFOoptions{#pdfoptions}

Opções de arquivo PDF.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`processo`*` | `xsd:string` | Opção de &quot;processos PDF&quot;. |
| `*`resolução`*` | `xsd:double` | Resolução do arquivo. |
| `*`colorspace`*` | `xsd:string` | Opção do Modo de espaço de cores pós-script. |
| `*`pdfCatalog`*` | `xsd:boolean` | Se um PDF de várias páginas deve ser combinado em um eCatalog após a renderização (o padrão é true). |
| `*`extractSearchWords`*` | `xsd:boolean` | Se as palavras de pesquisa devem ser extraídas do arquivo PDF. |
| `*`extractLinks`*` | `xsd:boolean` | Se os links PDF devem ser extraídos em mapas de imagem atribuídos às páginas rasterizadas no IPS. |

