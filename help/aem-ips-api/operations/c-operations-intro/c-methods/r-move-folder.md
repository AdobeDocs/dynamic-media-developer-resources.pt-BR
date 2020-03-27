---
description: Mova uma pasta para um novo local.
seo-description: Mova uma pasta para um novo local.
seo-title: moveFolder
solution: Experience Manager
title: moveFolder
topic: Scene7 Image Production System API
uuid: 424858c3-5796-4ae9-b5ad-fd50ddbee702
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# moveFolder{#movefolder}

Mova uma pasta para um novo local.

Sintaxe

## Tipos de usuário autorizados {#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-473c2e68bcc14a9ea2593bee26e679dd}

**Entrada (moveFolderParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sim | Segure a empresa. |
| ` *`folderHandle`*` | `xsd:string` | Sim | Identificador da pasta. |
| ` *`destFolderHandle`*` | `xsd:string` | Sim | Manipule a pasta de destino. |

**Saída (moveFolderReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Sim | Manipule a pasta movida. |

## Exemplos {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**Solicitação**

```java
<moveFolderParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <companyHandle>c|101</companyHandle>
   <folderHandle>f|test/MoveTest/</folderHandle>
   <destFolderHandle>f|DevanCo/DestFolder/</destFolderHandle>
</moveFolderParam>
```

**Resposta**

```java
<moveFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <folderHandle>f|test/DestFolder/MoveTest/</folderHandle>
</moveFolderReturn>
```

