---
description: Atribuir ou atualizar ativos em um projeto.
seo-description: Atribuir ou atualizar ativos em um projeto.
seo-title: setProjectAssets
solution: Experience Manager
title: setProjectAssets
topic: Scene7 Image Production System API
uuid: 98d18948-d387-4890-9c27-e8ab60cded1d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setProjectAssets{#setprojectassets}

Atribuir ou atualizar ativos em um projeto.

Sintaxe

## Tipos de usuário autorizados {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**Entrada (setProjectAssetsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`companyName`*` | `xsd:string` | Sim | Alça da Empresa. |
| ` *`projectHandle`*` | `xsd:string` | Sim | Manuseio do projeto. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Sim | A matriz de identificadores de ativos que você deseja associar ao projeto. |

**Saída (setProjectAssetsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Sim | O número de ativos adicionados com êxito. |

## Exemplos {#section-33c1a909c3dc4aa98da474c23a036596}

Essa amostra de código atribui um ativo a um projeto. A solicitação retorna uma contagem de sucesso de um.

**Solicitação**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**Resposta**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```

