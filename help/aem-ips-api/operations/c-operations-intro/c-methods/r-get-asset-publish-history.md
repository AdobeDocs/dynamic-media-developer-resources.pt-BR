---
description: Retorna o histórico de publicação de um ativo.
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
TQID: 'https://experienceleague.adobe.com/fXYa2SsttVpR9a1bebJ1oouyK8peSZ5GdgldPqU9s1g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 89
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
| companyHandle | `xsd:string` | Sim | O identificador da empresa com o histórico de publicação do ativo. |
| assetHandle | `xsd:string` | Sim | O ativo com o histórico de publicação que você deseja examinar. |

**Saída (getAssetPublishHistoryReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| pubHistoryArray | `types:PublishHistoryArray` | Sim | O histórico de publicação do ativo. |

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

