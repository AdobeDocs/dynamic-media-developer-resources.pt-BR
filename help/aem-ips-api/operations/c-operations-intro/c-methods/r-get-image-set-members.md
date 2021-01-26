---
description: Obtém uma matriz de membros que estão em um conjunto de imagens.
seo-description: Obtém uma matriz de membros que estão em um conjunto de imagens.
seo-title: getImageSetMembers
solution: Experience Manager
title: getImageSetMembers
topic: Dynamic Media Image Production System API
uuid: b19c9fec-df92-42e1-9228-42cdf196fdfc
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---


# getImageSetMembers{#getimagesetmembers}

Obtém uma matriz de membros que estão em um conjunto de imagens.

Sintaxe

## Tipos de usuário autorizados {#section-eaa3a167fa77403ea1b374b05fff4ded}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Requer acesso de leitura à imagem e ao ativo do conjunto de membros.

## Parâmetros {#section-a67ba98095574533980997c83ceaa316}

**Entrada (getImageSetMembersParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | A alça da empresa que contém o conjunto de imagens. |
| `*`assetHandle`*` | `xsd:string` | Sim | O identificador do ativo do conjunto de imagens. |

**Saída (getImageSetMembersReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`memberArray`*` | `types:ImageSetMemberArray` | Não | Matriz de membros do conjunto de imagens. |

## Exemplos {#section-888a9a78033346f39b171229de93dfa0}

Essa amostra de código retorna membros específicos do conjunto de imagens. A resposta retorna uma matriz vazia.

**Solicitação**

```java
<ns1:getImageSetMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>34195|22|927</ns1:assetHandle>
</ns1:getImageSetMembersParam>
```

**Resposta**

```java
<getImageSetMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray></memberArray>
</getImageSetMembersReturn>
```

