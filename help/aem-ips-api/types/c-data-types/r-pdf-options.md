---
description: Opções de arquivo do PDF.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
TQID: 'https://experienceleague.adobe.com/gjd-g7jhWVbLRL3kYnkX96ihjkiK34oCp7Ns1iC89GM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 0%

---

# [!DNL PDFOptions]{#pdfoptions}

Opções de arquivo do PDF.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| processo | `xsd:string` | Escolha de &quot;processos PDF&quot;. |
| resolution | `xsd:double` | Resolução do arquivo. |
| colorspace | `xsd:string` | Opção de Modo Colorspace pós-script. |
| pdfCatalog | `xsd:boolean` | Se um PDF de várias páginas deve ser combinado em um eCatalog após a renderização (o padrão é verdadeiro). |
| extractSearchWords | `xsd:boolean` | Se as palavras de pesquisa devem ser extraídas do arquivo PDF. |
| extractLinks | `xsd:boolean` | Se os links do PDF devem ser extraídos em mapas de imagem atribuídos às páginas rasterizadas no IPS. |
