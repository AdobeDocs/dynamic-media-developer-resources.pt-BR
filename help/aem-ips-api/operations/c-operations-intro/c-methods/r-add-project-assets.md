---
description: Adiciona um ou mais ativos a um projeto.
solution: Experience Manager
title: addProjectAssets
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---


# addProjectAssets{#addprojectassets}

Adiciona um ou mais ativos a um projeto.

Sintaxe

## Tipos de usuário autorizados {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-20d498e971b6466298e60c8a77fc32b2}

**Entrada (addProjectAssetsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Lida com a empresa associada ao projeto atual. |
| `*`projectHandle`*` | `xsd:string` | Sim | Lide com o projeto ao qual você está adicionando ativos. |
| `*`projectHandleArray`*` | `xsd:HandleArray` | Sim | Matriz de ativos que você está adicionando ao projeto atual. |

**Saída (addProjectAssetsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sim | O número de ativos adicionados com êxito. |
| `*`warningCount`*` | `xsd:int` | Sim | O número de avisos gerados quando a operação tentou adicionar ativos a um projeto. |
| `*`errorCount`*` | `xsd:int` | Sim | O número de erros gerados quando a operação tentou adicionar ativos a um projeto. |
| `*`warningDetailHandle`*` | `xsd:AssetOperationFaultArray` | Não | Matriz de avisos gerados por ativos quando a operação tentou adicioná-los a um projeto. |
| `*`companyHandle`*` | `xsd:AssetOperationFaultArray` | Não | Matriz de erros gerados por ativos quando a operação tentou adicioná-los a um projeto. |

## Exemplos {#section-bee5be2402f54cb9a3a02cc07def4135}

Este exemplo adiciona um único ativo (referenciado pelo identificador) em uma matriz de identificador de ativo a um projeto especificado na solicitação. A operação foi concluída com êxito quando a resposta `successCount` retorna `1`.

**Solicitação**

```java
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**Resposta**

```java
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```

