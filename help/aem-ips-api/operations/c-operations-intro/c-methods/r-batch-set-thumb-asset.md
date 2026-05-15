---
description: Define a imagem em miniatura de um ou mais ativos.
solution: Experience Manager
title: batchSetThumbAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f7d7ddd9-a3c3-47c4-8da6-d693851d0d7f
TQID: 'https://experienceleague.adobe.com/bANJIeE9iNsdm0RevvIgeU--faqAqmUyeZRJn09Oieg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 171
ht-degree: 0%

---

# batchSetThumbAsset{#batchsetthumbasset}

Define a imagem em miniatura de um ou mais ativos.

Sintaxe

## Tipos de ativos em miniatura {#section-4edc2a6a8f824213b0aaddb1d437268c}

Os tipos de ativos de miniatura permitidos consistem no seguinte:

* Imagem
* ModoDeExibiçãoAjustado
* Máscara
* Modelo
* PsdTemplate

## Tipos de usuário autorizados {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura/gravação ao ativo de destino e acesso de leitura ao ativo thumb.

## Parâmetros {#section-9c6efa000b384b3db6c013def20cf40b}

**Entrada (batchSetThumbAssetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa que contém os ativos. |
| updateArray | `types:ThumbAssetUpdateArray` | Sim | A matriz de atualizações. |

**Saída (batchSetThumbAssetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| successCount | `xsd:int` | Sim | O número de miniaturas definidas com êxito. |
| warningCount | `xsd:int` | Sim | O número de avisos gerados quando a operação tentou definir as miniaturas. |
| errorCount | `xsd:int` | Sim | O número de erros gerados quando a operação tentou definir as miniaturas. |
| warningDetailArray | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram avisos quando a operação tentou aplicar as atualizações. |
| errorDetailArray | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram erros quando a operação tentou aplicar as atualizações. |

## Exemplos {#section-6de69a8680c24c1486c5f01488393381}

**Solicitação**

```java
<batchSetThumbAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|234</assetHandle>
         <thumbAssetHandle>a|189</thumbAssetHandle>
      </items>
   </updateArray>
```

**Resposta**

```java
<batchSetThumbAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetThumbAssetReturn>
```
