---
description: Obtém uma matriz de membros que estão em um conjunto de imagens.
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic, SDK/API, Conjuntos de imagens
role: Developer,Administrator
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '101'
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
>Requer acesso de leitura à imagem e ao conjunto de membros.

## Parâmetros {#section-a67ba98095574533980997c83ceaa316}

**Entrada (getImageSetMembersParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém o conjunto de imagens. |
| `*`assetHandle`*` | `xsd:string` | Sim | O identificador de ativo do conjunto de imagens. |

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
