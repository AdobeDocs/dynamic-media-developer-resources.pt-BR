---
description: Arquivo hierárquico ou objeto de armazenamento de ativo. As pastas podem conter uma (ou mais) subpastas.
seo-description: Arquivo hierárquico ou objeto de armazenamento de ativo. As pastas podem conter uma (ou mais) subpastas.
seo-title: Pasta
solution: Experience Manager
title: Pasta
topic: Scene7 Image Production System API
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Pasta{#folder}

Arquivo hierárquico ou objeto de armazenamento de ativo. As pastas podem conter uma (ou mais) subpastas.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Identificador da pasta. |
| ` *`caminho`*` | `xsd:string` | Caminho da pasta. |
| ` *`lastModified`*` | `xsd:dateTime` | Data da última modificação. |
| ` *`childLastModified`*` | `xsd:dateTime` | Data da última modificação para subpastas e ativos filho da pasta. |
| ` *`permissionsSetHandle`*` | `xsd:string` | O identificador de permissões da pasta. |
| ` *`hasSubfolder`*` | `types:Boolean` | Determina se uma pasta tem subpastas. |
| ` *`subfolderArray`*` | `types:FolderArray` | Uma matriz de subpastas em uma pasta. |

