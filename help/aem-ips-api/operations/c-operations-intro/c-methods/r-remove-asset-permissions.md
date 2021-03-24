---
description: Remove permissões de ativos selecionados.
solution: Experience Manager
title: removeAssetPermissions
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '77'
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
| `*`companyHandle`*` | `xsd:string` | Sim | O nome da empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | O identificador do ativo com permissões que você deseja remover. |

**Saída (removeAssetPermissionsReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-238fa7bb091548f5ba72ced11fc92d4f}

Esta amostra de código remove as permissões de um ativo.

**Solicitação**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**Resposta**

Nenhum.
