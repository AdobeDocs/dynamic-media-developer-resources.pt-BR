---
description: Move um ativo para uma pasta específica.
solution: Experience Manager
title: moveAsset
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Developer,Administrator
exl-id: c5357c1a-92ac-4f9c-957e-b62cb812796c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

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
| `*`companyHandle`*` | `xsd:string` | Sim | Manipule a empresa. |
| `*`assetHandle`*` | `xsd:string` | Sim | Manipule o ativo que deseja mover. |
| `*`folderHandle`*` | `xsd:string` | Sim | Lide com a pasta de destino. |

**Saída (moveAssetReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-78333769f4f14e2886fdf06433c9d2ad}

Essa amostra de código move um ativo para uma pasta.

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
