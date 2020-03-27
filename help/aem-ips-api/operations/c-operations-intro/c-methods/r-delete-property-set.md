---
description: Exclui um conjunto de propriedades e todas as propriedades associadas.
seo-description: Exclui um conjunto de propriedades e todas as propriedades associadas.
seo-title: deletePropertySet
solution: Experience Manager
title: deletePropertySet
topic: Scene7 Image Production System API
uuid: b4fdf51f-89ec-4a69-9179-078ee8e1937f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`setHandle`*` | `xsd:string` | Sim | O identificador do conjunto de propriedades a ser excluído. |

**Saída (deletePropertySetParam)**

A API IPS não retorna uma resposta para esta operação.

## Exemplos {#section-cf319fc8f86a40ab9cbd838b031973fe}

Esta amostra de código usa o identificador do conjunto como um campo no `deletePropertySetParam` enviado para o servidor de serviços da Web IPS para excluir o conjunto de propriedades.

**Solicitação**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**Resposta**

Nenhum.
