---
description: Define metadados de ativos usando o modo de lote.
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
TQID: 'https://experienceleague.adobe.com/MQA1ShXDX9EUPfR9LolEVhA6F52W71gGZI75miE7uRs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 0%

---

# batchSetAssetMetadata{#batchsetassetmetadata}

Define metadados de ativos usando o modo de lote.

Sintaxe

## Tipos de usuário autorizados {#section-5310d9fd00604cbf9756944900378855}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-7111ac93bc7747f69ba14db4ac3912b0}

**Entrada (batchSetAssetMetadataParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | O identificador da empresa cujos metadados você deseja definir em uma operação em lote. |
| updateArray | `types:BatchMetadataUpdateArray` | Sim | A matriz de atualizações de metadados aplicadas aos ativos. |

**Saída (batchSetAssetMetadataParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| successCount | `xsd:int` | Sim | O número de metadados definidos com êxito. |
| warningCount | `xsd:int` | Sim | O número de avisos gerados quando a operação tentou definir metadados. |
| errorCount | `xsd:int` | Sim | O número de erros gerados quando a operação tentou definir metadados. |
| warningDetailArray | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geram avisos quando a operação tentou definir metadados em lote para os ativos. |
| errorDetailArray | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geram erros quando a operação tentou definir metadados em lote para os ativos. |

## Exemplos {#section-2de798ac920e4b47b971b1729a64395b}

**Solicitação**

```java {.line-numbers}
<batchSetAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
<companyHandle>c|6</companyHandle>
<updateArray>
   <items>
      <assetHandleArray>
         <items>a|743|1|538</items>
         <items>a|744|1|539</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>400</value>
         </items>
      </updateArray>
   </items>
   <items>
      <assetHandleArray>
         <items>a|732|1|535</items>
         <items>a|739|1|537</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>300</value>
         </items>
      </updateArray>
   </items>
</updateArray>
</batchSetAssetMetadataParam>
```

**Resposta**

```java {.line-numbers}
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```

