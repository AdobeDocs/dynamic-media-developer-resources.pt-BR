---
description: Mova uma pasta para um novo local.
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

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
| `*`companyHandle`*` | `xsd:string` | Sim | Manipule a empresa. |
| `*`folderHandle`*` | `xsd:string` | Sim | Identificador de pasta. |
| `*`destFolderHandle`*` | `xsd:string` | Sim | Lide com a pasta de destino. |

**Saída (moveFolderReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Sim | Lide com a pasta movida. |

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

