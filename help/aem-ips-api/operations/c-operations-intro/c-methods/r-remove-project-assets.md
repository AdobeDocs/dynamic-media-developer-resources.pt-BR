---
description: Remove ativos de um projeto. Não destrói os ativos.
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---


# removeProjectAssets{#removeprojectassets}

Remove ativos de um projeto. Não destrói os ativos.

Sintaxe

## Tipos de usuário autorizados {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-169d8e317417415b87df86242f65710e}

**Entrada (removeProjectAssetsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O controle da empresa com os ativos que deseja mover. |
| `*`projectHandle`*` | `xsd:string` | Sim | O identificador dos ativos do projeto que deseja mover. |
| `*`assetHandleArray`*` | `types:HandleArray` | Sim | Matriz de ativos que você deseja mover. |

**Saída (removeProjectAssetsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sim | Contagem de ativos removida com êxito. |
| `*`warningCount`*` | `xsd:int` | Sim | O número de avisos gerados quando a operação tentou remover ativos do projeto. |
| `*`errorCount`*` | `xsd:int` | Sim | O número de erros gerados quando a operação tentou remover ativos do projeto. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram avisos quando a operação tentou removê-los do projeto. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram erros quando a operação tentou removê-los do projeto. |

## Exemplos {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

Esta amostra de código remove 2 ativos de um projeto (especificado pelo identificador do projeto).

**Solicitação**

```java
<removeProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
      <items>a|739|1|537</items>
   </assetHandleArray>
</removeProjectAssetsParam>
```

