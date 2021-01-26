---
description: Define a imagem em miniatura de um ou mais ativos.
seo-description: Define a imagem em miniatura de um ou mais ativos.
seo-title: batchSetThumbAsset
solution: Experience Manager
title: batchSetThumbAsset
topic: Dynamic Media Image Production System API
uuid: 16c298a7-bb07-4643-824b-8f864d7f0290
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---


# batchSetThumbAsset{#batchsetthumbasset}

Define a imagem em miniatura de um ou mais ativos.

Sintaxe

## Tipos de ativos miniatura {#section-4edc2a6a8f824213b0aaddb1d437268c}

Os tipos de ativos em miniatura permitidos consistem no seguinte:

* Imagem
* AjustedView
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
>O usuário deve ter acesso de leitura/gravação ao ativo do público alvo e acesso de leitura ao ativo de thumb.

## Parâmetros {#section-9c6efa000b384b3db6c013def20cf40b}

**Entrada (batchSetThumbAssetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa que contém os ativos. |
| `*`updateArray`*` | `types:ThumbAssetUpdateArray` | Sim | A matriz de atualizações. |

**Saída (batchSetThumbAssetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sim | O número de miniaturas definidas com êxito. |
| `*`warningCount`*` | `xsd:int` | Sim | O número de avisos gerados quando a operação tentou definir as miniaturas. |
| `*`errorCount`*` | `xsd:int` | Sim | O número de erros gerados quando a operação tentou definir as miniaturas. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram avisos quando a operação tentou aplicar as atualizações. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram erros quando a operação tentou aplicar as atualizações. |

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

