---
description: Estatísticas de espaço em disco para um ativo ou pasta.
seo-description: Estatísticas de espaço em disco para um ativo ou pasta.
seo-title: DiskUsage
solution: Experience Manager
title: DiskUsage
topic: Dynamic Media Image Production System API
uuid: a63f0ed0-c689-43b0-9c3e-9500715d15a5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 0%

---


# DiskUsage{#diskusage}

Estatísticas de espaço em disco para um ativo ou pasta.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Alça da empresa. |
| `*`companyName`*` | `xsd:string` | Nome da empresa. |
| `*`imageCount`*` | `xsd:int` | Número de imagens armazenadas. |
| `*`diskSpaceUsage`*` | `xsd:long` | Total do lado do arquivo em quilobytes. |
| `*`lastModified`*` | `xsd:dateTime` | Data, hora e fuso horário em que o tipo `DiskUsage` foi modificado pela última vez. |

