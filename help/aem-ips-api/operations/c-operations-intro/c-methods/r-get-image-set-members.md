---
description: Obtém uma matriz de membros que estão em um conjunto de imagens.
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
TQID: 'https://experienceleague.adobe.com/7tS3wEIqaBPmykuVmDBfq9GugDcbnevj-XAQQHM3icY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
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
| companyHandle | `xsd:string` | Sim | O identificador da empresa que contém o conjunto de imagens. |
| assetHandle | `xsd:string` | Sim | O identificador do ativo do conjunto de imagens. |

**Saída (getImageSetMembersReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| memberArray | `types:ImageSetMemberArray` | Não | Matriz de membros do conjunto de imagens. |

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
