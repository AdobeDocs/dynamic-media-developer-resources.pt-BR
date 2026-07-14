---
description: Atribuir ou atualizar ativos em um projeto.
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6e6e9bd-5ee2-4750-9182-49e7a3e3486c
TQID: 'https://experienceleague.adobe.com/J5X6PS7L7YCH6J9ClzAUo24O44fMWxNqPnILckRBbUI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 0%

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
| companyName | `xsd:string` | Sim | Identificador da empresa. |
| projectHandle | `xsd:string` | Sim | Identificador de projeto. |
| assetHandleArray | `types:HandleArray` | Sim | A matriz de manipuladores de ativos que você deseja associar ao projeto. |

**Saída (setProjectAssetsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| successCount | `xsd:int` | Sim | O número de ativos adicionados com sucesso. |

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

