---
description: Arquivo hierárquico ou objeto de armazenamento de ativo. As pastas podem conter uma (ou mais) subpastas.
solution: Experience Manager
title: Pasta
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
TQID: 'https://experienceleague.adobe.com/nh6zqOnt-bxAFmsHSHPRCMThKlOwi-9b9fep6ujKZyE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 70
ht-degree: 0%

---

# [!DNL Folder]{#folder}

Arquivo hierárquico ou objeto de armazenamento de ativo. As pastas podem conter uma (ou mais) subpastas.

Sintaxe

## Parâmetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrição |
|---|---|---|
| folderHandle | `xsd:string` | Identificador de pasta. |
| [!DNL path] | `xsd:string` | Caminho da pasta. |
| lastModified | `xsd:dateTime` | Data da última modificação. |
| childLastModified | `xsd:dateTime` | Data da última modificação para subpastas e ativos secundários da pasta. |
| permissionsSetHandle | `xsd:string` | Identificador de permissões de pasta. |
| hasSubfolder | `types:Boolean` | Determina se uma pasta tem subpastas. |
| subfolderArray | `types:FolderArray` | Uma matriz de subpastas em uma pasta. |
