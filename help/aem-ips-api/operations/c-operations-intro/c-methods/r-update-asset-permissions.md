---
description: Atualiza as permissões do ativo.
solution: Experience Manager
title: updateAssetPermissions
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Developer,Administrator
exl-id: 12972a52-7b70-405c-9c73-e5ce6ab7dd9b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 0%

---

# updateAssetPermissions{#updateassetpermissons}

Atualiza as permissões do ativo.

Sintaxe

## Tipos de usuário autorizados {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-392cb3076cf84790a32fd913f2b111a3}

**Entrada (updateAssetPermissionsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Manuseio da empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | Identificador de ativo. |
| `*`updateArray`*` | `types:PermissionUpdateArray` | Sim | Permissões que você deseja aplicar ao ativo. |

**Saída (updateAssetPermissionsReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-1b7b7dbfdab34c819a53f3d33004e1f9}

**Solicitação**

```java
<ns1:updateAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>false</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateAssetPermissionsParam>
```

**Resposta**

Nenhum.
