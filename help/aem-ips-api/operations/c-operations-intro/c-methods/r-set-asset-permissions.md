---
description: Define as permissões de um único ativo usando um ativo de permissão.
seo-description: Define as permissões de um único ativo usando um ativo de permissão.
seo-title: setAssetPermissions
solution: Experience Manager
title: setAssetPermissions
uuid: 38f26482-bce9-4d2c-9714-e8c3ae40c2d1
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# setAssetPermissions{#setassetpermissions}

Define as permissões de um único ativo usando um ativo de permissão.

Por padrão, os ativos herdam as permissões da pasta pai. Depois de definir permissões em um ativo, elas não herdam mais as permissões do pai, a menos que você chame `removeAssetPermissions`.

## Tipos de usuário autorizados {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-e05abbce6453450fb38747101cb5e228}

**Entrada (setAssetPermissionsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém a pasta com a qual deseja trabalhar. |
| `*`assetHandle`*` | `xsd:string` | Sim | Identificador de pasta. |
| `*`permissionArray`*` | `types:PermissionsUpdateArray` | Sim | Matriz de permissões. |

**Saída (setAssetPermissionsReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-38955bc330bb4909b6b06027ef2b143e}

Este exemplo de código define permissões em um ativo. Ele contém a empresa e o identificador de ativos e um storage de permissões.

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
