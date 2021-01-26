---
description: Define as permissões de um único ativo usando um ativo de permissão.
seo-description: Define as permissões de um único ativo usando um ativo de permissão.
seo-title: setAssetPermissions
solution: Experience Manager
title: setAssetPermissions
topic: Dynamic Media Image Production System API
uuid: 38f26482-bce9-4d2c-9714-e8c3ae40c2d1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# setAssetPermissions{#setassetpermissions}

Define as permissões de um único ativo usando um ativo de permissão.

Por padrão, os ativos herdam as permissões de sua pasta pai. Depois de definir permissões em um ativo, ele não herda mais as permissões do pai, a menos que você chame `removeAssetPermissions`.

## Tipos de usuário autorizados {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-e05abbce6453450fb38747101cb5e228}

**Entrada (setAssetPermissonsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém a pasta com a qual você deseja trabalhar. |
| `*`assetHandle`*` | `xsd:string` | Sim | Identificador da pasta. |
| `*`permissionsArray`*` | `types:PermissionsUpdateArray` | Sim | Matriz de permissões. |

**Saída (setAssetPermissonsReturn)**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-38955bc330bb4909b6b06027ef2b143e}

Esta amostra de código define permissões em um ativo. Ele contém a empresa e o identificador de ativos e um storage de permissões.

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
