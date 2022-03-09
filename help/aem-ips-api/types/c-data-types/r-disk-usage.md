---
description: Estatísticas de espaço em disco para um ativo ou pasta.
solution: Experience Manager
title: Uso de disco
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 0%

---

# Uso de disco{#diskusage}

Estatísticas de espaço em disco para um ativo ou pasta.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| companyHandle | `xsd:string` | Manuseio da empresa. |
| companyName | `xsd:string` | Nome da empresa. |
| imageCount | `xsd:int` | Número de imagens armazenadas. |
| diskSpaceUsage | `xsd:long` | Lado total do arquivo em kilobytes. |
| lastModified | `xsd:dateTime` | Data, hora e fuso horário na `DiskUsage` foi modificado pela última vez. |
