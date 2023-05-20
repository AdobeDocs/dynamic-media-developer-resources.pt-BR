---
description: Define as permissões de um único ativo usando um ativo de permissão.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# setAssetPermissions{#setassetpermissions}

Define as permissões de um único ativo usando um ativo de permissão.

Por padrão, os ativos herdam as permissões da pasta principal. Depois de definir permissões em um ativo, ele não herda mais as permissões de seu pai, a menos que você chame `removeAssetPermissions`.

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

**Saída (setAssetPermissionsReturn)**

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
