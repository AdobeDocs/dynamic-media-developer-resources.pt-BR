---
description: Verifica se há conflitos de ID de IPS comparando os nomes de ativos com todos os nomes do namespace de catálogo do Servidor de imagens/Renderização de imagens de uma empresa.
solution: Experience Manager
title: checkAssetNames
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0756c4fc-64ec-4022-a6aa-fcf1542b41b0
TQID: 'https://experienceleague.adobe.com/RbFXhRqcaGXLMAeJhXMzho-ylSe2ktcKwvdbFtrcppM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 0%

---

# checkAssetNames{#checkassetnames}

Verifica se há conflitos de ID de IPS comparando os nomes de ativos com todos os nomes do namespace de catálogo do Servidor de imagens/Renderização de imagens de uma empresa.

Sintaxe

## Tipos de usuário autorizados {#section-8efcbb3f555f417a870219e4714374db}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`
* `TrialSiteAdmin`
* `TrialSiteUser`

## Parâmetros {#section-9c75b00f2072453abea0bdefc6ad7c99}

**Entrada (checkAssetNamesParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Não | O identificador da empresa que contém o usuário. |
| assetNamesArray | `types:StringArray` | Sim | Uma matriz de nomes de ativos a serem verificados. |

**Saída (checkAssetNamesReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| inUseNameArray | `types:StringArray` | Sim | Uma matriz de nomes de ativos em uso. |

## Exemplos {#section-bc5d120d74614a63a425ca3acc337219}

Este código de amostra solicita os nomes de ativos em uso para uma empresa especificada. A resposta retorna uma matriz de nomes de ativos que estão em uso.

**Solicitação**

```java
<checkAssetNamesParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <companyHandle>c|1</companyHandle>
   <assetNameArray>
      <items>ABC123</items>
      <items>DEF456</items>
   </assetNameArray>
</checkAssetNamesParam>
```

**Resposta**

```java
<checkAssetNamesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-09-10">
   <inUseNameArray>
      <items>DEF456</items>
   </inUseNameArray>
</checkAssetNamesReturn>
```
