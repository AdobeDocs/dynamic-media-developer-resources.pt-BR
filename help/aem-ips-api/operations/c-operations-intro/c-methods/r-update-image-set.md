---
description: Atualiza um conjunto de imagens.
seo-description: Atualiza um conjunto de imagens.
seo-title: updateImageSet
solution: Experience Manager
title: updateImageSet
topic: Dynamic Media Image Production System API
uuid: df118ba3-d86f-4005-928e-76a5a9f899fc
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---


# updateImageSet{#updateimageset}

Atualiza um conjunto de imagens.

Sintaxe

## Parâmetros {#section-3be47dbbce474ce78676b05e163492e3}

**Entrada (updateImageSetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém o conjunto de imagens que você deseja modificar. |
| `*`assetHandle`*` | `xsd:string` | Sim | O identificador do conjunto de imagens que você deseja modificar. |
| `*`memberArray`*` | `types:ImageSetMemberUpdateArray` | Não | Redefine os membros do conjunto de imagens. |
| `*`thumbAssetHandle`*` | `xsd:string` | Não | O identificador do ativo que atua como a miniatura do conjunto de imagens. |

**Saída (updateImageSetReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`sequência`*` |  |  |  |

## Exemplos {#section-ce47a4b6e062423fa55ed3a0fd26d7ff}

**Solicitação**

```java
<updateImageSetParam xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"> 
  <companyHandle>c|15</companyHandle> 
  <assetHandle>a|381</assetHandle> 
  <memberArray> 
    <items> 
      <assetHandle>a|374</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|375</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
    <items> 
      <assetHandle>a|376</assetHandle> 
      <pageReset>false</pageReset> 
    </items> 
  </memberArray> 
  <thumbAssetHandle>a|376</thumbAssetHandle> 
</updateImageSetParam>
```

**Resposta**

```java
<updateImageSetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2014-04-03"/>
```

