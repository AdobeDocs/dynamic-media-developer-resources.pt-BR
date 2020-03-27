---
description: Move um ativo para uma pasta específica.
seo-description: Move um ativo para uma pasta específica.
seo-title: moveAsset
solution: Experience Manager
title: moveAsset
topic: Scene7 Image Production System API
uuid: cabeb7b7-ab0b-44d0-ad90-623f76e4323d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# moveAsset{#moveasset}

Move um ativo para uma pasta específica.

Sintaxe

## Tipos de usuário autorizados {#section-e4f2d2a58132450aa36da6377134211e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-dd0bbdf293aa4563af70a91f97c861f1}

**Entrada (moveAssetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sim | Segure a empresa. |
| ` *`assetHandle`*` | `xsd:string` | Sim | Manipule o ativo que deseja mover. |
| ` *`folderHandle`*` | `xsd:string` | Sim | Manipule a pasta de destino. |

**Saída (moveAssetReturn)**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-78333769f4f14e2886fdf06433c9d2ad}

Esta amostra de código move um ativo para uma pasta.

**Solicitação**

```java
<ns1:moveAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24266|1|17062</ns1:assetHandle>
   <ns1:folderHandle>MyCompany/My New Images/</ns1:folderHandle>
</ns1:moveAssetParam>
```

**Resposta**

Nenhum.
