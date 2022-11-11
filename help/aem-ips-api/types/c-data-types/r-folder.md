---
description: Arquivo hierárquico ou objeto de armazenamento de ativos. As pastas podem conter uma (ou mais) subpastas.
solution: Experience Manager
title: Pasta
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 0%

---

# [!DNL Folder]{#folder}

Arquivo hierárquico ou objeto de armazenamento de ativos. As pastas podem conter uma (ou mais) subpastas.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| folderHandle | `xsd:string` | Identificador de pasta. |
| [!DNL path] | `xsd:string` | Caminho da pasta. |
| lastModified | `xsd:dateTime` | Data da última modificação. |
| childLastModified | `xsd:dateTime` | Última data de modificação para subpastas e ativos filho da pasta. |
| permissionsSetHandle | `xsd:string` | Identificador de permissões de pasta. |
| hasSubfolder | `types:Boolean` | Determina se uma pasta tem subpastas. |
| subfolderArray | `types:FolderArray` | Uma matriz de subpastas em uma pasta. |
