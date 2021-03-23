---
description: Retorna pastas e subpastas em uma estrutura de árvore hierárquica. A resposta getFolderTree é limitada a no máximo 100.000 pastas
seo-description: Retorna pastas e subpastas em uma estrutura de árvore hierárquica. A resposta getFolderTree é limitada a no máximo 100.000 pastas
seo-title: getFolderTree
solution: Experience Manager
title: getFolderTree
uuid: 93fda0d6-c656-4254-b07b-7a448e164f28
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---


# getFolderTree{#getfoldertree}

Retorna pastas e subpastas em uma estrutura de árvore hierárquica. A resposta getFolderTree é limitada a no máximo 100.000 pastas

Sintaxe

## Tipos de usuário autorizados {#section-66ef19149f4d4123a3a99004b5a2743e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura à pasta para retornar os dados nela.

## Parâmetros {#section-0c2b30513f1e439cbd840e8cc6465b3a}

**Entrada (getFolderTreeParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O nome da empresa. |
| `*`accessUserHandle`*` | `xsd:string` | Não | Usado apenas por administradores para representar um usuário específico. |
| `*`accessGroupHandle`*` | `xsd:string` | Não | Usado para filtrar por um grupo específico, incluindo qualquer um daqueles aos quais a empresa pertence. |
| `*`folderPath`*` | `xsd:string` | Não | A pasta raiz para recuperar pastas e todas as subpastas para o nível da folha. Se for excluída, a raiz da empresa será usada. |
| `*`profundidade`*` | `xsd:int` | Sim | Um valor zero obtém a pasta de nível superior. Qualquer outro valor especifica a profundidade a ser descendente na árvore. |
| `*`assetTypeArray`*` | `types:StringArray` | Não | Retorna pastas que contêm apenas os tipos de ativos especificados. |
| `*`responseFieldArray`*` | `types:StringArray` | Não | Contém uma lista de campos que você deseja incluir na resposta. |
| `*`excludeFieldArray`*` | `types:StringArray` | Não | Contém uma lista de campos que você deseja excluir na resposta. |

**Saída (getFolderTreeReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`pastas`*` | `types:folders` | Não | A hierarquia de pastas em uma estrutura de árvore. A resposta é limitada a no máximo 100.000 pastas. |
| `*`permissionSetArray`*` | `types:PermissionSetArray` |  |  |

## Exemplos {#section-a9fd2edb56574dd9bf8b0f2fd89367e4}

Essa amostra de código usa um identificador da empresa e um parâmetro de profundidade para determinar o nível de profundidade que a resposta deve retornar. A resposta contém pastas e matrizes de subpastas com relacionadas. Defina o valor de profundidade para um número menor para pesquisar mais fundo na árvore de pastas.

**Solicitação**

```java
<ns1:getFolderTreeParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:depth>-1</ns1:depth>
</ns1:getFolderTreeParam>
```

**Resposta**

```java
<getFolderTreeReturn xmlns="http://www.scene7.com/IpsApi/xsd/">
  <folders>
    <items>
      <folderHandle>f|sampleFolder/uploadTestDir/</folderHandle>
      <path>MyCompany/uploadTestDir/</path>
      <lastModified>2011-11-14T11:19:59.031-08:00</lastModified>
      <childLastModified>2011-11-14T11:19:59.031-08:00</childLastModified>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <hasSubfolders>true</hasSubfolders>
      <subfolderArray>
        <items>
          <folderHandle>f|MyCompany/uploadTestDir/SubFolder/</folderHandle>
          <path>DevanCo/uploadTestDir/SubFolder/</path>
          <lastModified>2011-11-14T11:19:59.032-08:00</lastModified>
          <childLastModified>2011-11-14T11:19:59.032-08:00</childLastModified>
          <permissionSetHandle>pm|2</permissionSetHandle>
          <hasSubfolders>true</hasSubfolders>
          <subfolderArray>
            <items>
              <folderHandle>f|MyCompany/uploadTestDir/SubFolder/10/</folderHandle>
              <path>DevanCo/uploadTestDir/SubFolder/10/</path>
              <lastModified>2011-11-14T11:19:59.033-08:00</lastModified>
              <childLastModified>2011-11-14T15:06:58.563-08:00</childLastModified>
              <permissionSetHandle>pm|2</permissionSetHandle>
              <hasSubfolders>false</hasSubfolders>
            </items>
          </subfolderArray>
        </items>
      </subfolderArray>
    </items>
  </folders>
  <permissionSetArray>
    <items>
      <permissionSetHandle>pm|2</permissionSetHandle>
      <permissionArray>
        <items>
          <groupHandle>g|1</groupHandle>
          <groupName>Asset Download Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>false</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Read</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
        <items>
          <groupHandle>g|2</groupHandle>
          <groupName>Asset Upload Group</groupName>
          <permissionType>Write</permissionType>
          <isAllowed>true</isAllowed>
          <isOverride>true</isOverride>
        </items>
      </permissionArray>
    </items>
  <permissionSetArray>
</getFolderTreeReturn>
```

