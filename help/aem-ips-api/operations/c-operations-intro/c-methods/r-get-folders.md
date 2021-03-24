---
description: Retorna todas as pastas e subpastas, começando no caminho da pasta. A resposta getFolders retorna no máximo 100.000 pastas.
solution: Experience Manager
title: getFolders
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---


# getFolders{#getfolders}

Retorna todas as pastas e subpastas, começando no caminho da pasta. A resposta getFolders retorna no máximo 100.000 pastas.

## Propósito das pastas {#section-66e344d5333f42f1b060a0cba25935c3}

Uma pasta permite organizar subpastas e ativos. Todos os nomes de pasta e ativo devem ser exclusivos. Pastas e ativos que compartilham o mesmo nome causarão um conflito de namespace, mesmo se estiverem em hierarquias de pastas diferentes.
Sintaxe

## Tipos de usuário autorizados {#section-0dc7e17cb60f4cf7bcdb76648e5d2f8e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura à pasta para retornar os dados nela.

## Parâmetros {#section-0c1976503eaa418a9226b51667901176}

**Entrada (getFoldersParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O nome da empresa. |
| `*`accessUserHandle`*` | `xsd:string` | Não | Usado pelos administradores para representar um usuário específico. |
| `*`accessGroupHandle`*` | `xsd:string` | Não | Filtrar por um grupo específico. |
| `*`folderPath`*` | `xsd:string` | Não | A pasta raiz para recuperar pastas e todas as subpastas para o nível da folha. Se for excluída, a raiz da empresa será usada. |
| `*`assetTypeArray`*` | `types:StringArray` | Não | Retorna pastas que contêm apenas os tipos de ativos especificados. |
| `*`responseFieldArray`*` | `types:StringArray` | Não | Contém uma lista de campos que você deseja incluir na resposta. |
| `*`excludeFieldArray`*` | `types:StringArray` | Não | Contém uma lista de campos que você deseja excluir da resposta. |

**Saída (getFoldersReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`folderArray`*` | `types:FolderArray` | Não | Uma matriz de pastas que correspondem aos critérios de filtro. A resposta é limitada a 100.000 pastas no máximo. |
| `*`permissionsSetArray`*` | `types:PermissionSetArray` |  |  |

## Exemplos {#section-b5cb06e9fb9945ad898dbdc3692b754e}

Essa amostra de código retorna uma matriz que contém todas as pastas de uma empresa, juntamente com informações específicas sobre cada pasta.

**Solicitação**

```java
<ns1:getFoldersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getFoldersParam>
```

**Resposta**

```java
<getFoldersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderArray>
      <items>
         <folderHandle>MyCompany/</folderHandle>
         <path>MyCompany/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/eCatalogs/</folderHandle>
         <path>MyCompany/eCatalogs/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
      <items>
         <folderHandle>MyCompany/PDF/</folderHandle>
         <path>MyCompany/PDF/</path>
         <hasSubfolders>false</hasSubfolders>
      </items>
   </folderArray>
</getFoldersReturn>
```

