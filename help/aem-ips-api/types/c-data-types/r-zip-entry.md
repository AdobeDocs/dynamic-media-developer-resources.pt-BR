---
description: Uma entrada em um arquivo ZIP.
seo-description: Uma entrada em um arquivo ZIP.
seo-title: ZipEntry
solution: Experience Manager
title: ZipEntry
uuid: 05aac11b-249c-4c44-943d-fa6bf35d3637
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 1%

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

