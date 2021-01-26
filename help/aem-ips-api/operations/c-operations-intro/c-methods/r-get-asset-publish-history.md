---
description: Retorna o histórico de publicação de um ativo.
seo-description: Retorna o histórico de publicação de um ativo.
seo-title: getAssetPublishHistory
solution: Experience Manager
title: getAssetPublishHistory
topic: Dynamic Media Image Production System API
uuid: 15025c3d-eac3-4cb8-9a2a-fd80bd67478f
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---


# getAssetPublishHistory{#getassetpublishhistory}

Retorna o histórico de publicação de um ativo.

Sintaxe

## Tipos de usuário autorizados {#section-3b9d6a129093458fa8890139a2718912}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-3541bd9914a44b89acfc1d419b560ee6}

**Entrada (getAssetPublishHistoryParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa com o histórico de publicação do ativo. |
| `*`assetHandle`*` | `xsd:string` | Sim | O ativo com o histórico de publicação que você deseja examinar. |

**Saída (getAssetPublishHistoryReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`pubHistoryArray`*` | `types:PublishHistoryArray` | Sim | O histórico de publicação do ativo. |

## Exemplos {#section-53897c51e5a047c5bd5ea5a6efb2d114}

Essa amostra de código retorna o histórico de publicação de um ativo. Um ativo nunca foi publicado se o servidor retornar uma matriz vazia.

**Solicitação**

```java
<getAssetPublishHistoryParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetPublishHistoryParam>
```

**Resposta**

```java
<getAssetPublishHistoryReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <pubHistoryArray/>
</getAssetPublishHistoryReturn>
```

