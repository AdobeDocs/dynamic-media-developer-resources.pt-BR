---
description: Obtém os ativos e o número de ativos associados a uma empresa específica.
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# getAssetCounts{#getassetcounts}

Obtém os ativos e o número de ativos associados a uma empresa específica.

O `countArray` retornado consiste em uma matriz de `assetTypes` (tipo de dados) `xsd:string`), cada um com seu próprio campo de contagem (tipo de dados `xsd:int`), permitindo a representação de vários tipos de ativos por elemento da matriz.
Sintaxe

## Tipos de usuário autorizados {#section-6234754722184e828352f10eb18fbce9}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-2a9581315eca427d8a3d26cc3fca7b1f}

**Entrada (getAssetCountsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa com ativos que você deseja contar. |

**Saída (getAssetCountsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| countArray | `types:AssetCountArray` | Não | Uma matriz de tipos de ativos, cada um com seu próprio campo de contagem, permitindo a representação de vários tipos de ativos por elemento da matriz. |

## Exemplos {#section-6052a503eb3843f6adb99e200fdba280}

Essa amostra de código usa o identificador da empresa como um campo no `getAssetCountsParam` enviado ao servidor de serviços Web IPS para obter as contagens de ativos.

**Solicitação**

```java
<getAssetCountsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
</getAssetCountsParam>
```

**Resposta**

```java
<getAssetCountsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <countArray>
      <items>
         <assetType>Image</assetType>
         <count>44</count>
      </items>
      <items>
         <assetType>Flash</assetType>
         <count>3</count>
      </items>
   </countArray>
</getAssetCountsReturn>
```
