---
description: Arquivo hierárquico ou objeto de armazenamento de ativos. As pastas podem conter uma (ou mais) subpastas.
solution: Experience Manager
title: Pasta
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
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

