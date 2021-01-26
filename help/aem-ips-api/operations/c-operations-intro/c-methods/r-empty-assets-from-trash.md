---
description: Esvazia ativos da lixeira IPS.
seo-description: Esvazia ativos da lixeira IPS.
seo-title: emptyAssetsFromTrash
solution: Experience Manager
title: emptyAssetsFromTrash
topic: Dynamic Media Image Production System API
uuid: de11a7b0-cd4b-4717-8596-d39afbcf7e9c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---


# emptyAssetsFromTrash{#emptyassetsfromtrash}

Esvazia ativos da lixeira IPS.

Os ativos vivem no lixo até serem esvaziados manualmente ou até saírem do lixo. Se forem esvaziados manualmente, vivem na Lixeira até o próximo trabalho de limpeza (normalmente à noite) quando são finalmente removidos do sistema. Se saírem do lixo, os ativos são limpos como parte da mesma atividade de limpeza. O tempo limite é configurável (o padrão é 7 dias).

## Tipos de usuário autorizados {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* &quot;

## Parâmetros {#section-8e1fb0ee3aae453581e99ef76e298569}

**Entrada (emptyAssetsFromTrashParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sim | O identificador da empresa proprietária dos ativos. |
| `*`assetHandleArray`*` | `types:HandleArray` | Sim | A matriz de alças que representam os itens a serem esvaziados do lixo. |

**Saída (emptyAssetsFromTrashParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`successCount`*` | `xsd:Int` | Sim | O número de ativos esvaziados com êxito do lixo. |
| `*`warningCount`*` | `xsd:Int` | Sim | O número de avisos gerados quando a operação tentou esvaziar ativos do lixo. |
| `*`errorCount`*` | `xsd:Int` | Sim | O número de erros gerados quando a operação tentou esvaziar ativos do lixo. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram avisos quando a operação tentou esvaziá-los da lixeira. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram erros quando a operação tentou esvaziá-los da lixeira. |

## Exemplos {#section-6154a873b6c342bf92e2036280cafdcf}

Essa amostra de código usa o identificador da empresa e um storage de identificador de ativo que contém identificadores para os ativos a serem esvaziados da lixeira.

**Solicitação**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Resposta**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```

