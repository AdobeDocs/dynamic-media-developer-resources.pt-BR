---
description: Atualiza um conjunto de ativos.
solution: Experience Manager
title: updateAssetSet
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: af7899c4-a95f-42c8-858e-ed1592c6f5b6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# updateAssetSet{#updateassetset}

Atualiza um conjunto de ativos.

Sintaxe

## Parâmetros {#section-d7080ccd97334c94860eb107a3e132b2}

**Entrada (updateAssetSetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa que contém o conjunto de imagens que você deseja modificar. |
| assetHandle | `xsd:string` | Sim | O identificador do conjunto de imagens que você deseja modificar. |
| setDefinition | `xsd:string` | Não | Redefine os membros do conjunto de imagens. |
| thumbAssetHandle | `xsd:string` | Não | O identificador do ativo que atua como a miniatura do conjunto de imagens. |

**Saída (updateAssetSetReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
|  |  |  |  |

## Exemplos {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Solicitação**

```java
<updateAssetSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|535</assetHandle> 
  <setDefinition>${getCatalogId([a|202])};${getCatalogId([a|202])};advanced_image;,${getCatalogId([a|935])};${getCatalogId([a|935])};advanced_image;,${getCatalogId([a|933])};${getCatalogId([a|933])};advanced_image;</setDefinition> 
  <thumbAssetHandle>a|202</thumbAssetHandle> 
</updateAssetSetParam>
```

**Resposta**

```java
<updateAssetSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```
