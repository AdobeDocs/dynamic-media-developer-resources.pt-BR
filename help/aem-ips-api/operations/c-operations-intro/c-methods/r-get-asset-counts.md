---
description: Obtém os ativos e o número de ativos associados a uma empresa específica.
seo-description: Obtém os ativos e o número de ativos associados a uma empresa específica.
seo-title: getAssetCount
solution: Experience Manager
title: getAssetCount
topic: Dynamic Media Image Production System API
uuid: 92103806-59da-444f-b69c-d045d0ebf42e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# getAssetCount{#getassetcounts}

Obtém os ativos e o número de ativos associados a uma empresa específica.

O `countArray` retornado consiste em uma matriz de `assetTypes` (tipo de dados `xsd:string`), cada uma com seu próprio campo de contagem (tipo de dados `xsd:int`), permitindo a representação de vários tipos de ativos por elemento da matriz.
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
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa com ativos que você deseja contar. |

**Saída (getAssetCountReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`countArray`*` | `types:AssetCountArray` | Não | Uma matriz de tipos de ativos, cada um com seu próprio campo de contagem, permitindo a representação de vários tipos de ativos por elemento da matriz. |

## Exemplos {#section-6052a503eb3843f6adb99e200fdba280}

Esta amostra de código usa o identificador da empresa como um campo no `getAssetCountsParam` enviado para o servidor de serviços Web IPS para obter as contagens de ativos.

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

