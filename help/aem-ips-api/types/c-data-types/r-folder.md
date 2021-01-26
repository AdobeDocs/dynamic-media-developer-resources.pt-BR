---
description: Arquivo hierárquico ou objeto de armazenamento de ativo. As pastas podem conter uma (ou mais) subpastas.
seo-description: Arquivo hierárquico ou objeto de armazenamento de ativo. As pastas podem conter uma (ou mais) subpastas.
seo-title: Pasta
solution: Experience Manager
title: Pasta
topic: Dynamic Media Image Production System API
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# Pasta{#folder}

Arquivo hierárquico ou objeto de armazenamento de ativo. As pastas podem conter uma (ou mais) subpastas.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Identificador da pasta. |
| `*`caminho`*` | `xsd:string` | Caminho da pasta. |
| `*`lastModified`*` | `xsd:dateTime` | Data da última modificação. |
| `*`childLastModified`*` | `xsd:dateTime` | Data da última modificação para subpastas e ativos filho da pasta. |
| `*`permissionsSetHandle`*` | `xsd:string` | O identificador de permissões da pasta. |
| `*`hasSubfolder`*` | `types:Boolean` | Determina se uma pasta tem subpastas. |
| `*`subfolderArray`*` | `types:FolderArray` | Uma matriz de subpastas em uma pasta. |

