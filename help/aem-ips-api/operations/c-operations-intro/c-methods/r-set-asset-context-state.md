---
description: Defina ou atualize o estado de publicação de um ou mais ativos. É possível definir estados de publicação separados para cada contexto de publicação em uma empresa.
solution: Experience Manager
title: setAssetsContextState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 28d0a67b-3e36-43fc-800d-17c841dca3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 0%

---

# setAssetsContextState{#setassetscontextstate}

Defina ou atualize o estado de publicação de um ou mais ativos. É possível definir estados de publicação separados para cada contexto de publicação em uma empresa.

## Tipos de usuário autorizados {#section-815eb031f85143278c1560c18c5e3431}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura para retornar o ativo.

## Parâmetros {#section-009b9006de8e4c16ad657c47f28ace9f}

**Entrada (setAssetsContextStateParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | `xsd:string` | Sim | Processe a empresa. |
| assetsContextHandle | `types:AssetsContextStateUpdateArray` | Sim | Uma matriz de ativos e seus novos estados de publicação. |

**Saída (setAssetsContexStateReturn)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| successCount | `xsd:int` | Sim | O número de ativos alterados com sucesso. |
| warningCount | `xsd:int` | Sim | O número de avisos gerados quando a operação tentou modificar ativos. |
| errorCount | `xsd:int` | Sim | O número de erros gerados quando a operação tentou modificar ativos. |
| warningDetailArray | `types:AssetOperationFaultArray` | Não | Matriz de erros gerados por ativos quando a operação tentou modificá-los. |

## Exemplos {#section-283a073f3cb14bcda5abed863c538aa4}

Esta amostra de código define o estado de publicação de um ativo usando `NotMarkedForPublish`.

**Solicitação**

```java
<setAssetsContextStateParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetsContextStateUpdateArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
  </assetsContextStateUpdateArray>
</setAssetsContextStateParam>
```

**Resposta**

```java
<setAssetsContextStateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04-beta">
  <successCount>8</successCount>
  <warningCount>0</warningCount>
  <errorCount>0</errorCount>
</setAssetsContextStateReturn>
```
