---
description: Remove permissões de ativos selecionados.
seo-description: Remove permissões de ativos selecionados.
seo-title: removeAssetPermissions
solution: Experience Manager
title: removeAssetPermissions
topic: Dynamic Media Image Production System API
uuid: 5a351862-f412-4d89-90b7-9e70a26eacbc
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 0%

---


# removeAssetPermissions{#removeassetpermissions}

Remove permissões de ativos selecionados.

Sintaxe

## Tipos de usuário autorizados {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**Entrada (removeAssetPermissionsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | A alça da empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | O identificador do ativo com permissões que você deseja remover. |

**Saída (removeAssetPermissionsReturn)**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-238fa7bb091548f5ba72ced11fc92d4f}

Esta amostra de código remove permissões de um ativo.

**Solicitação**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**Resposta**

Nenhum.
