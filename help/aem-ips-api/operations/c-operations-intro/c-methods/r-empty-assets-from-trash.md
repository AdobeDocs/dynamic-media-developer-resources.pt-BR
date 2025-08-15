---
title: emptyAssetsFromTrash
description: Esvazia os ativos da lixeira de IPS.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 36866dc8-6a16-4445-942f-d0ea3c168272
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# emptyAssetsFromTrash{#emptyassetsfromtrash}

Esvazia os ativos da lixeira de IPS.

O Assets fica no lixo até que sejam esvaziados manualmente ou até que desapareçam do lixo. Se forem esvaziados manualmente, eles permanecerão na Lixeira até o próximo trabalho de limpeza (normalmente à noite), quando finalmente forem removidos do sistema. Se o tempo limite for esgotado, os ativos serão apagados como parte dessa mesma atividade de limpeza. O tempo limite pode ser configurado (o padrão é 7 dias).

## Tipos de usuário autorizados {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parâmetros {#section-8e1fb0ee3aae453581e99ef76e298569}

**Entrada (emptyAssetsFromTrashParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| companyHandle | xsd:string | Sim | O identificador da empresa que detém os ativos. |
| assetHandleArray | tipos:HandleArray | Sim | O conjunto de manipuladores que representam os itens a serem esvaziados da lixeira. |

**Saída (emptyAssetsFromTrashParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| successCount | xsd:Int | Sim | O número de ativos esvaziados com êxito da lixeira. |
| warningCount | xsd:Int | Sim | O número de avisos gerados quando a operação tentou esvaziar ativos da lixeira. |
| errorCount | xsd:Int | Sim | O número de erros gerados quando a operação tentou esvaziar ativos da lixeira. |
| warningDetailArray | tipos:AssetOperationFaultArray | Não | A matriz de detalhes associados aos ativos que geraram avisos quando a operação tentou esvaziá-los da lixeira. |
| errorDetailArray | tipos:AssetOperationFaultArray | Não | A matriz de detalhes associados aos ativos que geraram erros quando a operação tentou esvaziá-los da lixeira. |

## Exemplos {#section-6154a873b6c342bf92e2036280cafdcf}

Esta amostra de código usa o identificador da empresa e uma matriz de identificadores de ativos que contém identificadores para os ativos a serem esvaziados da lixeira.

**Solicitação**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Resposta**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2023-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```
