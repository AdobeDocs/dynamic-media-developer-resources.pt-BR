---
description: Retorna uma matriz de nomes de caminho Photoshop para a imagem fornecida.
solution: Experience Manager
title: getPhotoshopPathNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 11d4c0d0-a3a3-4324-a4a6-1dd7b7e673da
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# getPhotoshopPathNames{#getphotoshoppathnames}

Retorna uma matriz de nomes de caminho Photoshop para a imagem fornecida.

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
| companyHandle | `xsd:string` | Sim | Processe a empresa que contém a imagem com a qual você deseja trabalhar. |
| assetHandle | `xsd:string` | Sim | Processe o ativo de imagem. |

**Saída (getPhotoshopPathNamesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| pathNameArray | `types:StringArray` | Sim | Uma matriz de nomes de caminho Photoshop em uma imagem. |

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
