---
description: Exclui um conjunto de propriedades e todas as propriedades associadas.
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 72429030-200d-4e13-a537-10a728998a26
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 0%

---

# deletePropertySet{#deletepropertyset}

Exclui um conjunto de propriedades e todas as propriedades associadas.

Sintaxe

## Tipos de usuário autorizados {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parâmetros {#section-e5fc868f69494cf6858e03027db09101}

**Entrada (deletePropertySetParam)**

| Nome | Tipo | Obrigatório | Descrição |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | Sim | O identificador do conjunto de propriedades a ser excluído. |

**Saída (deletePropertySetParam)**

A API do IPS não retorna uma resposta para esta operação.

## Exemplos {#section-cf319fc8f86a40ab9cbd838b031973fe}

Este exemplo de código usa o identificador do conjunto como um campo no `deletePropertySetParam` enviado ao servidor de serviços Web IPS para excluir o conjunto de propriedades.

**Solicitação**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Resposta**

Nenhum.
