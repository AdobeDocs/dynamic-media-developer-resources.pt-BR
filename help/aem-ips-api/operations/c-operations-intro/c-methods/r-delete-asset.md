---
description: Exclui um ativo.
seo-description: Exclui um ativo.
seo-title: deleteAsset
solution: Experience Manager
title: deleteAsset
uuid: 47f700e0-04bf-4d33-a18a-d938f7e9e326
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Desenvolvedor,Administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
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
