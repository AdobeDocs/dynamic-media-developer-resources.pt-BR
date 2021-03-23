---
description: Renomeia uma pasta.
seo-description: Renomeia uma pasta.
seo-title: renameFolder
solution: Experience Manager
title: renameFolder
uuid: 7d190a57-1d81-4f41-9205-b8ffdf7330ec
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
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
| `*`companyHandle`*` | `xsd:string` | Sim | Manipule para a empresa com as pastas que deseja renomear. |
| `*`folderHandle`*` | `xsd:string` | Sim | Lide com a pasta . |
| `*`folderName`*` | `xsd:string` | Sim | Novo nome da pasta. |

**Saída (renameFolderReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Sim | Lida com a pasta renomeada. |

## Exemplos {#section-98bdd2f88d164f488676e90aba1dc864}

Essa amostra de código renomeia uma pasta.

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

