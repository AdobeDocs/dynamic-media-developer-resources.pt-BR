---
description: Define as permissões de um único ativo usando um ativo de permissão.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
TQID: 'https://experienceleague.adobe.com/dd96ai2DgoCqZ1NR-2rixSHDEaBSgk6ioQIqmG-1RoE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 0%

---

# setAssetPermissions{#setassetpermissions}

Define as permissões de um único ativo usando um ativo de permissão.

Por padrão, o Assets herda as permissões da pasta principal. Depois que você define permissões em um ativo, ele não herda mais as permissões de seu pai, a menos que você chame `removeAssetPermissions`.

## Tipos de usuário autorizados {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-e05abbce6453450fb38747101cb5e228}

**Entrada (setAssetPermissonsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa que contém a pasta com a qual você deseja trabalhar. |
| assetHandle | `xsd:string` | Sim | Identificador de pasta. |
| permissionArray | `types:PermissionsUpdateArray` | Sim | Matriz de permissões. |

**Saída (setAssetPermissonsReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-38955bc330bb4909b6b06027ef2b143e}

Esta amostra de código define permissões em um ativo. Ele contém a empresa, o identificador de ativos e uma matriz de permissões.

**Solicitação**

```java
<setAssetPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <assetHandle>97374|1|61046</assetHandle>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setAssetPermissionsParam>
```

**Resposta**

Nenhum.

