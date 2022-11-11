---
description: Opções de arquivo PDF.
solution: Experience Manager
title: PDFOoptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---

# [!DNL PDFOptions]{#pdfoptions}

Opções de arquivo PDF.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| processo | `xsd:string` | Escolha de &quot;PDF processes&quot;. |
| resolution | `xsd:double` | Resolução de arquivo. |
| colorspace | `xsd:string` | Opção de Modo Colorspace Pós-script. |
| pdfCatalog | `xsd:boolean` | Combinar um PDF de várias páginas em um eCatalog após a renderização (o padrão é verdadeiro). |
| extractSearchWords | `xsd:boolean` | Se as palavras de pesquisa devem ser extraídas do arquivo PDF. |
| extractLinks | `xsd:boolean` | Se os links PDF devem ser extraídos em mapas de imagem atribuídos às páginas rasterizadas no IPS. |
