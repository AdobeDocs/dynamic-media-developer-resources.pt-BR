---
description: Define os metadados do ativo usando o modo de lote.
seo-description: Define os metadados do ativo usando o modo de lote.
seo-title: batchSetAssetMetadata
solution: Experience Manager
title: batchSetAssetMetadata
uuid: 88d8f279-988f-4956-b66f-60fa95cf511c
feature: Dynamic Media Classic, SDK/API, Metadata.Gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---


# batchSetAssetMetadata{#batchsetassetmetadata}

Define os metadados do ativo usando o modo de lote.

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
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa cujos metadados você deseja definir em uma operação em lote. |
| `*`updateArray`*` | `types:BatchMetadataUpdateArray` | Sim | A matriz de atualizações de metadados aplicadas aos ativos. |

**Saída (batchSetAssetMetadataParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sim | O número de metadados definidos com êxito. |
| `*`warningCount`*` | `xsd:int` | Sim | O número de avisos gerados quando a operação tentou definir metadados. |
| `*`errorCount`*` | `xsd:int` | Sim | O número de erros gerados quando a operação tentou definir metadados. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geram avisos quando a operação tentou fazer o conjunto de metadados em lote para os ativos. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geram erros quando a operação tentou colocar metadados em lote para os ativos. |

## Exemplos {#section-2de798ac920e4b47b971b1729a64395b}

**Solicitação**

```java
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

```java
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```

