---
description: Obtém os caminhos de arquivo originais dos ativos de uma empresa.
solution: Experience Manager
title: getOriginalFilePaths
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81d06a8c-55c1-47d5-adc9-928ab30199c6
TQID: 'https://experienceleague.adobe.com/D8lKzaqYSHdG-CXVAmlv5cuAuuEXEWlFSnqpiX8RkFI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 0%

---

# getOriginalFilePaths{#getoriginalfilepaths}

Obtém os caminhos de arquivo originais dos ativos de uma empresa.

Sintaxe

## Tipos de usuário autorizados {#section-da8d8561e9174e938f3595a5d6e50089}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Requer acesso de leitura ao ativo.

## Parâmetros {#section-a6b394daba6e49a8882cf3051035d9d1}

**Entrada (getOriginalFilePathsParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa. |
| assetHandleArray | `types:HandleArray` | Sim | Matriz de identificadores para ativos cujo caminho de arquivo original você deseja obter. |

**Saída (getOriginalFilePathsReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| originalFileArray | `types:StringArray` | Sim | A matriz de cadeias de caracteres que representam os caminhos do arquivo original. |

## Exemplos {#section-a966e783a2ba49f5b6b0f961329ab2f8}

Esta amostra de código retorna os caminhos de arquivo dos ativos especificados com identificadores de ativos exclusivos em uma matriz de identificadores de ativos.

**Solicitação**

```java
<ns1:getOriginalFilePathsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandleArray>
      <ns1:items>24265|1|17061</ns1:items>
      <ns1:items>24267|1|17063</ns1:items>
   </ns1:assetHandleArray>
</ns1:getOriginalFilePathsParam>
```

**Resposta**

```java
<getOriginalFilePathsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <originalFileArray>
      <items>MyCompany/Autumn Leaves.jpg</items>
      <items>MyCompany/Desert Landscape.jpg</items>
   </originalFileArray>
</getOriginalFilePathsReturn>
```
