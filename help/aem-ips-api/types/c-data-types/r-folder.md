---
description: Arquivo hierárquico ou objeto de armazenamento de ativos. As pastas podem conter uma (ou mais) subpastas.
solution: Experience Manager
title: Pasta
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# Pasta{#folder}

Arquivo hierárquico ou objeto de armazenamento de ativos. As pastas podem conter uma (ou mais) subpastas.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Identificador de pasta. |
| `*`caminho`*` | `xsd:string` | Caminho da pasta. |
| `*`lastModified`*` | `xsd:dateTime` | Data da última modificação. |
| `*`childLastModified`*` | `xsd:dateTime` | Última data de modificação para subpastas e ativos filho da pasta. |
| `*`permissionsSetHandle`*` | `xsd:string` | Identificador de permissões de pasta. |
| `*`hasSubfolder`*` | `types:Boolean` | Determina se uma pasta tem subpastas. |
| `*`subfolderArray`*` | `types:FolderArray` | Uma matriz de subpastas em uma pasta. |
