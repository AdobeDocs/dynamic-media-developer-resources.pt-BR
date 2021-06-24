---
description: Cria uma pasta.
solution: Experience Manager
title: createFolder
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# [!DNL createFolder]{#createfolder}

Cria uma pasta.

>[!NOTE]
>
>A nova pasta é secundária para a pasta Imagens, mesmo se você especificar um `/` para indicar a raiz da empresa.

Sintaxe

## Tipos de usuário autorizados {#section-14ef6368056b4e8f96198c20b6d93b9b}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura/gravação à pasta pai.

## Parâmetros {#section-c00d8d89cf114886a535056f2a1bf892}

**Entrada (createFolder)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O Identificador para a empresa |
| `*`folderPath`*` | `xsd:string` | Sim | A pasta raiz usada para recuperar pastas e todas as subpastas para o nível da folha. Se for excluída, a raiz da empresa será usada. |

**Saída (createFolderParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Sim | Manipule a nova pasta. |

## Exemplos {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Este código de amostra cria uma pasta na raiz de uma empresa. A resposta retorna o identificador da pasta recém-criada.

**Solicitação**

```java
<ns1:createFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderPath>/SpinSets</ns1:folderPath>
</ns1:createFolderParam>
```

**Resposta**

```java
<ns1:createFolderReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <folderHandle xmlns="http://www.scene7.com/IpsApi/xsd">MyCompany/SpinSets/</folderHandle>
</ns1:createFolderReturn>
```
