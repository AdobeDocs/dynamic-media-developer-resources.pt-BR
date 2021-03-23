---
description: Define valores de metadados para um ativo. Funciona com uma matriz de atualizações de metadados para definir valores em um lote.
seo-description: Define valores de metadados para um ativo. Funciona com uma matriz de atualizações de metadados para definir valores em um lote.
seo-title: setAssetMetadata
solution: Experience Manager
title: setAssetMetadata
uuid: 17fe8277-a164-4f91-af96-ea43d41bd4f2
feature: Dynamic Media Classic, SDK/API, metadados, gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '153'
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
