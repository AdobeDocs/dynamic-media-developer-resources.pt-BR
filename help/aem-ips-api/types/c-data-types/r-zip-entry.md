---
description: Uma entrada em um arquivo ZIP.
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '42'
ht-degree: 2%

---

# [!DNL ZipEntry]{#zipentry}

Uma entrada em um arquivo ZIP.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| name | `xsd:string` | Nome da entrada. |
| isDirectory | `xsd:boolean` | Determina se a entrada é um diretório. |
| lastModified | `xsd:dateTime` | Data e hora da última modificação. |
| compressedSize | `xsd:long` | Tamanho compactado. |
| uncompressedSize | `xsd:long` | Tamanho descompactado. |
