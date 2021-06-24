---
description: Define valores de metadados para um ativo. Funciona com uma matriz de atualizações de metadados para definir valores em um lote.
solution: Experience Manager
title: setAssetMetadata
feature: Dynamic Media Classic, SDK/API, metadados, gerenciamento de ativos
role: Developer,Administrator
exl-id: 811e44e1-774a-49bd-a2bd-a7504e5f7f5f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 0%

---

# setAssetMetadata{#setassetmetadata}

Define valores de metadados para um ativo. Funciona com uma matriz de atualizações de metadados para definir valores em um lote.

Sintaxe

## Tipos de usuário autorizados {#section-9dcacb0c924044648f8324bfed183dca}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura ao ativo.

## Parâmetros {#section-bcdcff30905e444388811e897b2824bd}

**Entrada (setAssetMetadataParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa com o ativo que deseja atualizar. |
| `*`assetHandle`*` | `xsd:string` | Sim | O identificador do ativo. |
| `*`updateArray`*` | `types:MetadataUpdateArray` | Sim | Atualizações em uma matriz de atualização de metadados. |

**Saída (setAssetMetadataReturn)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-1ab412e7ee1d4d6d8469b0b403598c42}

Este exemplo de código usa uma matriz de atualizações de metadados para definir os metadados do ativo especificado.

**Solicitação**

```java
<ns1:setAssetMetadataParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:fieldHandle>47|ALL|Resolution</ns1:fieldHandle>
         <ns1:value>320</ns1:value>
      </ns1:items>
   </ns1:updateArray>
</ns1:setAssetMetadataParam>
```

**Resposta**

Nenhum.
