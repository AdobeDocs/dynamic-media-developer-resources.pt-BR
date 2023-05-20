---
description: Renomeia uma pasta.
solution: Experience Manager
title: renameFolder
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 2d4f1059-8018-4efb-a1ec-8eb560b1a58f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 0%

---

# renameFolder{#renamefolder}

Renomeia uma pasta.

Sintaxe

## Tipos de usuário autorizados {#section-5a252b00937d4befbec76fa23fbae9df}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura e gravação ao ativo.

## Parâmetros {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**Entrada (renameFolderParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | Processe a empresa com as pastas que você deseja renomear. |
| folderHandle | `xsd:string` | Sim | Processe a pasta. |
| folderName | `xsd:string` | Sim | Nome da nova pasta. |

**Saída (renameFolderReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| folderHandle | `xsd:string` | Sim | Processe a pasta renomeada. |

## Exemplos {#section-98bdd2f88d164f488676e90aba1dc864}

Esta amostra de código renomeia uma pasta.

**Solicitação**

```java
<ns1:renameFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/PDF/</ns1:folderHandle>
   <ns1:folderName>My Newly Renamed PDF Folder</ns1:folderName>
</ns1:renameFolderParam>
```

**Resposta**

```java
<renameFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderHandle>MyCompany/My Newly Renamed PDF Folder/</folderHandle>
</renameFolderReturn>
```
