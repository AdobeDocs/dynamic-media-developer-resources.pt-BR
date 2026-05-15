---
description: Define as permissões da pasta.
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
TQID: 'https://experienceleague.adobe.com/r-WGRjE263vPSVKsBieklQ79SASbDQOx9hp5IzS0-O0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 91
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
| companyHandle | `xsd:string` | Sim | Identificador da empresa. |
| folderHandle | `xsd:string` | Sim | Identificador de pasta. |
| setChildren | `xsd:boolean` | Sim | Define permissões em filhos que pertencem à pasta. |
| permissionArray | `types:PermissionUpdateArray` | Sim | Matriz de permissões. |

**Saída (setFolderPermissionsReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-01730da4be874553ab44e3241cdf6357}

Esta amostra de código especifica um identificador de empresa, um identificador de pasta e uma matriz de permissões com informações detalhadas sobre a pasta. Ela aplica as mesmas permissões aos filhos da pasta principal.

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
