---
title: createFolder
description: Cria uma pasta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 569130ae-5515-4b14-a410-2bd6f9fc7638
TQID: 'https://experienceleague.adobe.com/iQNFDdsbxhklGSfUb1pmcNhzIT8kJYc19xFglU7Blc8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
ht-degree: 0%

---

# [!DNL createFolder]{#createfolder}

Cria uma pasta.

>[!NOTE]
>
>A nova pasta é subordinada à pasta Images, mesmo que você especifique um `/` para indicar a raiz da empresa.

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
>O usuário deve ter acesso de leitura/gravação à pasta principal.

## Parâmetros {#section-c00d8d89cf114886a535056f2a1bf892}

**Entrada (createFolder)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa |
| folderPath | `xsd:string` | Sim | A pasta raiz usada para recuperar pastas e todas as subpastas para o nível folha. Se excluída, a raiz da empresa é usada. |

**Saída (createFolderParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| folderHandle | `xsd:string` | Sim | Identificador da nova pasta. |

## Exemplos {#section-e596fbdb44fd43c8b30005cb2a2fdf26}

Este código de exemplo cria uma pasta na raiz de uma empresa. A resposta retorna o identificador da pasta recém-criada.

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
