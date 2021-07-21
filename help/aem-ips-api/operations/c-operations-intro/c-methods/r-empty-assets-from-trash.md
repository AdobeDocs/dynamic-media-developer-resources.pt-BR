---
description: Esvazia ativos da lixeira do IPS.
solution: Experience Manager
title: emptyAssetsFromTrash
feature: Dynamic Media Classic, SDK/API, Gerenciamento de ativos
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 0%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

Esvazia ativos da lixeira do IPS.

Os ativos vivem no lixo até serem manualmente esvaziados ou até ficarem fora do lixo. Se forem manualmente esvaziadas, elas ficarão na Lixeira até o próximo trabalho de limpeza (normalmente à noite), quando forem finalmente removidas do sistema. Se o tempo limite for excedido na lixeira, os ativos serão limpos como parte dessa mesma atividade de limpeza. O tempo limite é configurável (o padrão é 7 dias).

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
| `*`assetHandleArray`*` | `types:HandleArray` | Sim | A matriz de identificadores que representam os itens a serem esvaziados do lixo. |

**Saída (emptyAssetsFromTrashParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`successCount`*` | `xsd:Int` | Sim | O número de ativos esvaziados com êxito da lixeira. |
| `*`warningCount`*` | `xsd:Int` | Sim | O número de avisos gerados quando a operação tentou esvaziar ativos da lixeira. |
| `*`errorCount`*` | `xsd:Int` | Sim | O número de erros gerados quando a operação tentou esvaziar ativos da lixeira. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram avisos quando a operação tentou esvaziá-los da lixeira. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Não | A matriz de detalhes associados aos ativos que geraram erros quando a operação tentou esvaziá-los da lixeira. |

## Exemplos {#section-6154a873b6c342bf92e2036280cafdcf}

Este exemplo de código usa o identificador da empresa e uma matriz de manipulador de ativos que contém identificadores para os ativos a serem esvaziados da lixeira.

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
