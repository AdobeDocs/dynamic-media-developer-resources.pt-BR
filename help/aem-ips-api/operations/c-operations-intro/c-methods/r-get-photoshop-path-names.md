---
description: Retorna uma matriz de nomes de caminho do Photoshop para a imagem em questão.
seo-description: Retorna uma matriz de nomes de caminho do Photoshop para a imagem em questão.
seo-title: getPhotoshopPathNames
solution: Experience Manager
title: getPhotoshopPathNames
topic: Dynamic Media Image Production System API
uuid: d3f1dea5-393b-498e-963d-37a4e38068a2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 0%

---


# getPhotoshopPathNames{#getphotoshoppathnames}

Retorna uma matriz de nomes de caminho do Photoshop para a imagem em questão.

Sintaxe

## Tipos de usuário autorizados {#section-baa0fd4b92bc4ad89809efd659b3a629}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-605a4aab23104489a21f7f7f5849801b}

**Entrada (getPhotoshopPathNamesParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | Manuseie a empresa que contém a imagem com a qual você deseja trabalhar. |
| `*`assetHandle`*` | `xsd:string` | Sim | Lidar com o ativo de imagem. |

**Saída (getPhotoshopPathNamesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`pathNameArray`*` | `types:StringArray` | Sim | Uma matriz de nomes de caminho do Photoshop em uma imagem. |

## Exemplos {#section-6d316f14b4184d42af4ca3f717b042dd}

**Solicitação**

```java
<getPhotoshopPathNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <companyHandle>c|301</companyHandle>
  <assetHandle>a|26014</assetHandle>
</getPhotoshopPathNamesParam>
```

**Resposta**

```java
<getPhotoshopPathNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2012-07-31">
  <pathNameArray>
    <items>Background Path</items>
    <items>Face Path</items>
  </pathNameArray>
</getPhotoshopPathNamesReturn>
```

