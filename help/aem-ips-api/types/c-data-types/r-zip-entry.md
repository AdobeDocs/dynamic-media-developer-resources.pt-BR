---
description: Uma entrada em um arquivo ZIP.
seo-description: Uma entrada em um arquivo ZIP.
seo-title: ZipEntry
solution: Experience Manager
title: ZipEntry
topic: Dynamic Media Image Production System API
uuid: 05aac11b-249c-4c44-943d-fa6bf35d3637
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 2%

---


# ZipEntry{#zipentry}

Uma entrada em um arquivo ZIP.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`name`*` | `xsd:string` | Nome da entrada. |
| `*`isDirectory`*` | `xsd:boolean` | Determina se a entrada é um diretório. |
| `*`lastModified`*` | `xsd:dateTime` | Data e hora da última modificação. |
| `*`compressedSize`*` | `xsd:long` | Tamanho compactado. |
| `*`uncompressedSize`*` | `xsd:long` | Tamanho descompactado. |

