---
description: Verifica conflitos de ID IPS comparando os nomes dos ativos com todos os nomes de uma namespace de catálogo de Serviço de imagem/Renderização de imagem da empresa.
seo-description: Verifica conflitos de ID IPS comparando os nomes dos ativos com todos os nomes de uma namespace de catálogo de Serviço de imagem/Renderização de imagem da empresa.
seo-title: checkAssetNames
solution: Experience Manager
title: checkAssetNames
topic: Dynamic Media Image Production System API
uuid: 91d073a8-7648-429b-aa5c-c7d595550299
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# checkAssetNames{#checkassetnames}

Verifica conflitos de ID IPS comparando os nomes dos ativos com todos os nomes de uma namespace de catálogo de Serviço de imagem/Renderização de imagem da empresa.

Sintaxe

## Tipos de usuário autorizados {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Parâmetros {#section-9c75b00f2072453abea0bdefc6ad7c99}

**Entrada (checkAssetNamesParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Não | O identificador da empresa que contém o usuário. |
| `*`assetNamesArray`*` | `types:StringArray` | Sim | Uma matriz de nomes de ativos a serem verificados. |

**Saída (checkAssetNamesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`inUseNameArray`*` | `types:StringArray` | Sim | Uma matriz de nomes de ativos em uso. |

## Exemplos {#section-bc5d120d74614a63a425ca3acc337219}

Este exemplo de código solicita os nomes de ativos em uso para uma empresa especificada. A resposta retorna uma matriz de nomes de ativos que estão em uso.

**Solicitação**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**Resposta**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```

