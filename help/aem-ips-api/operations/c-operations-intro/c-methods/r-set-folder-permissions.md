---
description: Define as permissões da pasta.
seo-description: Define as permissões da pasta.
seo-title: setFolderPermissions
solution: Experience Manager
title: setFolderPermissions
topic: Dynamic Media Image Production System API
uuid: 3a33034e-df2c-48ab-8ade-b76bea444388
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# setFolderPermissions{#setfolderpermissions}

Define as permissões da pasta.

Sintaxe

## Tipos de usuário autorizados {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-2a41135054954396b40f1228f2e63b42}

**Entrada (setFolderPermissionsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Alça da empresa. |
| `*`folderHandle`*` | `xsd:string` | Sim | Identificador da pasta. |
| `*`setChildren`*` | `xsd:boolean` | Sim | Define permissões em filhos que pertencem à pasta. |
| `*`permissionsArray`*` | `types:PermissionUpdateArray` | Sim | Matriz de permissões. |

**Saída (setFolderPermissionsReturn)**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-01730da4be874553ab44e3241cdf6357}

Este exemplo de código especifica um identificador de empresa, um identificador de pasta e um storage de permissões com informações detalhadas sobre a pasta. Ela aplica as mesmas permissões aos filhos da pasta pai.

**Solicitação**

```java
<setFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <setChildren>true</setChildren>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setFolderPermissionsParam>
```

**Resposta**

Nenhum.
