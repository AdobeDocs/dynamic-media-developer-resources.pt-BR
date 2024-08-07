---
description: Adiciona um ou mais ativos a um projeto.
solution: Experience Manager
title: addProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 60aa2846-b41e-4131-b465-82aa832434f7
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '178'
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
| companyHandle | `xsd:string` | Sim | Processe a empresa associada ao projeto atual. |
| projectHandle | `xsd:string` | Sim | Identifique o projeto ao qual você está adicionando ativos. |
| projectHandleArray | `xsd:HandleArray` | Sim | Matriz de ativos que você está adicionando ao projeto atual. |

**Saída (addProjectAssetsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| successCount | `xsd:int` | Sim | O número de ativos adicionados com sucesso. |
| warningCount | `xsd:int` | Sim | O número de avisos gerados quando a operação tentou adicionar ativos a um projeto. |
| errorCount | `xsd:int` | Sim | O número de erros gerados quando a operação tentou adicionar ativos a um projeto. |
| warningDetailHandle | `xsd:AssetOperationFaultArray` | Não | Matriz de avisos gerados por ativos quando a operação tentou adicioná-los a um projeto. |
| companyHandle | `xsd:AssetOperationFaultArray` | Não | Matriz de erros gerados por ativos quando a operação tentou adicioná-los a um projeto. |

## Exemplos {#section-bee5be2402f54cb9a3a02cc07def4135}

Este exemplo adiciona um único ativo (referenciado por seu identificador) em uma matriz de identificador de ativo a um projeto especificado na solicitação. Operação concluída com êxito quando a resposta `successCount` retorna `1`.

**Solicitação**

```java {.line-numbers}
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**Resposta**

```java {.line-numbers}
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```
