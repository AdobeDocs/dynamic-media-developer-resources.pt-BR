---
description: Verifica conflitos de ID de IPS, comparando os nomes dos ativos com todos os nomes do namespace de catálogo de Exibição de imagem/Renderização de imagem de uma empresa.
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic, SDK/API
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---


# checkAssetNames{#checkassetnames}

Verifica conflitos de ID de IPS, comparando os nomes dos ativos com todos os nomes do namespace de catálogo de Exibição de imagem/Renderização de imagem de uma empresa.

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
| `*`companyHandle`*` | `xsd:string` | Não | O identificador para a empresa que contém o usuário. |
| `*`assetNamesArray`*` | `types:StringArray` | Sim | Uma matriz de nomes de ativos a serem verificados. |

**Saída (checkAssetNamesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`inUseNameArray`*` | `types:StringArray` | Sim | Uma matriz de nomes de ativos em uso. |

## Exemplos {#section-bc5d120d74614a63a425ca3acc337219}

Este código de exemplo solicita os nomes dos ativos em uso para uma empresa especificada. A resposta retorna uma matriz de nomes de ativos que estão em uso.

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

