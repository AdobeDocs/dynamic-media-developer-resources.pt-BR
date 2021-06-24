---
description: Exclui um ativo.
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Developer,Administrator
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# deleteAsset{#deleteasset}

Exclui um ativo.

Sintaxe

## Tipos de usuário autorizados {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>O usuário deve ter acesso de leitura e exclusão ao ativo.

## Parâmetros {#section-0eed164e278b456fbdfb7a50727a0416}

**Entrada (deleteAssetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa à qual a pasta pertence. |
| `*`assetHandle`*` | `xsd:string` | Sim | O identificador do ativo a ser excluído. |

**Saída (deleteAssetParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-d5657289f5234bb0a613dcf691507958}

Esse código de amostra exclui qualquer tipo de ativo de uma empresa específica. Requer um identificador de ativo, que deve ser obtido de outra operação.

**Solicitação**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**Resposta**

Nenhum.
